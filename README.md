<div align="center">
  <img src="https://github.com/fastify/graphics/raw/HEAD/fastify-landscape-outlined.svg" width="650" height="auto"/>
</div>

<div align="center">

[![CI](https://github.com/fastify/fastify/workflows/ci/badge.svg)](https://github.com/fastify/fastify/actions/workflows/ci.yml)
[![Coverage Status](https://coveralls.io/repos/github/fastify/fastify/badge.svg?branch=master)](https://coveralls.io/github/fastify/fastify?branch=master)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](http://standardjs.com/)
[![NPM version](https://img.shields.io/npm/v/fastify.svg?style=flat)](https://www.npmjs.com/package/fastify)
[![NPM downloads](https://img.shields.io/npm/dm/fastify.svg?style=flat)](https://www.npmjs.com/package/fastify) [![Discord](https://img.shields.io/discord/725613461949906985)](https://discord.gg/fastify)

</div>
<br />

# TL;DR

* [Fastify](https://github.com/fastify/fastify) is a fast and low overhead web framework for Node.js.
* This package shows how fast it is comparatively.
* For metrics (cold-start) see [metrics.md](./METRICS.md)

# Installing

```
npm i -g fastify-benchmarks
```

# Usage

```
benchmark [arguments (optional)]
```

#### Arguments

* `-h`: Help on how to use the tool.
* `compare`: Get comparative data for your benchmarks.

> You may also compare all test results, at once, in a single table; `benchmark compare -t`

> You can also extend the comparison table with percentage values based on fastest result; `benchmark compare -p`
# Benchmarks

* __Machine:__ linux x64 | 4 vCPUs | 15.6GB Mem
* __Node:__ `v14.21.3`
* __Run:__ Mon Aug 26 2024 02:29:06 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68939.6    | 14.01        | 12.29         |
| polkadot                 | 1.0.0   | ✗      | 67655.2    | 14.29        | 12.07         |
| h3                       | 0.8.6   | ✗      | 66174.8    | 14.59        | 10.86         |
| h3-router                | 0.8.6   | ✓      | 63441.6    | 15.29        | 10.41         |
| bare                     | 10.13.0 | ✗      | 61385.6    | 15.80        | 10.95         |
| restana                  | 4.9.9   | ✓      | 61379.2    | 15.79        | 10.95         |
| foxify                   | 0.10.20 | ✓      | 60634.4    | 15.99        | 9.95          |
| connect                  | 3.7.0   | ✗      | 59415.2    | 16.32        | 10.60         |
| polka                    | 0.5.2   | ✓      | 58240.0    | 16.68        | 10.39         |
| fastify                  | 4.28.1  | ✓      | 57872.8    | 16.78        | 10.38         |
| micro                    | 9.4.1   | ✗      | 56750.4    | 17.13        | 10.12         |
| server-base              | 7.1.32  | ✗      | 56624.8    | 17.16        | 10.10         |
| server-base-router       | 7.1.32  | ✓      | 55360.0    | 17.57        | 9.87          |
| yeps                     | 1.1.1   | ✗      | 53308.8    | 18.26        | 9.51          |
| connect-router           | 1.3.8   | ✓      | 51203.2    | 19.04        | 9.13          |
| trek-engine              | 1.0.5   | ✗      | 49787.2    | 19.59        | 8.17          |
| micro-route              | 2.5.0   | ✓      | 49492.0    | 19.70        | 8.83          |
| trek-router              | 1.2.0   | ✓      | 48546.4    | 20.11        | 7.96          |
| vapr                     | 0.6.0   | ✓      | 46752.0    | 20.89        | 7.67          |
| spirit                   | 0.6.1   | ✗      | 45245.6    | 21.66        | 8.07          |
| yeps-router              | 1.2.0   | ✓      | 44584.8    | 21.95        | 7.95          |
| spirit-router            | 0.5.0   | ✓      | 43580.0    | 22.45        | 7.77          |
| koa                      | 2.15.3  | ✗      | 43380.0    | 22.55        | 7.74          |
| total.js                 | 3.4.13  | ✓      | 40456.8    | 24.21        | 12.38         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40389.8    | 24.28        | 7.20          |
| take-five                | 2.0.0   | ✓      | 39831.8    | 24.60        | 14.32         |
| restify                  | 8.6.1   | ✓      | 39475.8    | 24.82        | 7.11          |
| koa-router               | 12.0.1  | ✓      | 38188.2    | 25.69        | 6.81          |
| hapi                     | 20.3.0  | ✓      | 34143.0    | 28.78        | 6.09          |
| microrouter              | 3.1.3   | ✓      | 32380.8    | 30.37        | 5.77          |
| trpc-router              | 9.27.4  | ✓      | 27112.0    | 36.38        | 6.00          |
| egg.js                   | 3.27.1  | ✓      | 17534.7    | 56.49        | 6.27          |
| express                  | 4.19.2  | ✓      | 13584.0    | 73.08        | 2.42          |
| fastify-big-json         | 4.28.1  | ✓      | 13193.6    | 75.25        | 151.79        |
| express-with-middlewares | 4.19.2  | ✓      | 12976.4    | 76.51        | 4.83          |
| express-route-prefix     | 4.19.2  | ✓      | 11103.2    | 89.49        | 4.11          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

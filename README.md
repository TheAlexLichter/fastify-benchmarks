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
* __Run:__ Mon Jan 20 2025 02:37:20 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69972.4    | 13.79        | 12.48         |
| polkadot                 | 1.0.0   | ✗      | 67658.8    | 14.29        | 12.07         |
| h3-router                | 0.8.6   | ✓      | 65341.6    | 14.80        | 10.72         |
| h3                       | 0.8.6   | ✗      | 63131.6    | 15.35        | 10.36         |
| restana                  | 4.9.9   | ✓      | 61120.0    | 15.86        | 10.90         |
| bare                     | 10.13.0 | ✗      | 60679.2    | 15.99        | 10.82         |
| foxify                   | 0.10.20 | ✓      | 59937.6    | 16.19        | 9.83          |
| polka                    | 0.5.2   | ✓      | 59110.4    | 16.42        | 10.54         |
| connect                  | 3.7.0   | ✗      | 57616.8    | 16.86        | 10.28         |
| micro                    | 9.4.1   | ✗      | 57555.2    | 16.88        | 10.26         |
| fastify                  | 4.29.0  | ✓      | 56192.8    | 17.29        | 10.08         |
| server-base-router       | 7.1.32  | ✓      | 55979.2    | 17.37        | 9.98          |
| server-base              | 7.1.32  | ✗      | 55334.4    | 17.57        | 9.87          |
| yeps                     | 1.1.1   | ✗      | 52538.4    | 18.54        | 9.37          |
| connect-router           | 1.3.8   | ✓      | 50694.4    | 19.23        | 9.04          |
| micro-route              | 2.5.0   | ✓      | 49342.4    | 19.77        | 8.80          |
| trek-router              | 1.2.0   | ✓      | 48806.4    | 20.00        | 8.01          |
| trek-engine              | 1.0.5   | ✗      | 48773.6    | 20.01        | 8.00          |
| vapr                     | 0.6.0   | ✓      | 46644.0    | 20.94        | 7.65          |
| spirit-router            | 0.5.0   | ✓      | 44808.8    | 21.82        | 7.99          |
| spirit                   | 0.6.1   | ✗      | 44183.2    | 22.14        | 7.88          |
| yeps-router              | 1.2.0   | ✓      | 43386.4    | 22.55        | 7.74          |
| koa                      | 2.15.3  | ✗      | 43089.6    | 22.70        | 7.68          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39951.2    | 24.53        | 7.12          |
| total.js                 | 3.4.13  | ✓      | 39428.8    | 24.86        | 12.07         |
| restify                  | 8.6.1   | ✓      | 39342.6    | 24.91        | 7.09          |
| take-five                | 2.0.0   | ✓      | 38605.4    | 25.41        | 13.88         |
| koa-router               | 12.0.1  | ✓      | 38203.0    | 25.67        | 6.81          |
| hapi                     | 20.3.0  | ✓      | 33631.2    | 29.24        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 32344.6    | 30.41        | 5.77          |
| trpc-router              | 9.27.4  | ✓      | 27383.2    | 36.01        | 6.06          |
| egg.js                   | 3.30.1  | ✓      | 17667.7    | 56.07        | 6.32          |
| express                  | 4.21.2  | ✓      | 13570.4    | 73.12        | 2.42          |
| fastify-big-json         | 4.29.0  | ✓      | 12700.8    | 78.21        | 146.12        |
| express-with-middlewares | 4.21.2  | ✓      | 12346.4    | 80.44        | 4.59          |
| express-route-prefix     | 4.21.2  | ✓      | 10946.8    | 90.77        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

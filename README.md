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
* __Run:__ Mon Jun 16 2025 03:08:24 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69011.6    | 13.99        | 12.31         |
| 0http                    | 3.5.3   | ✓      | 68251.2    | 14.15        | 12.17         |
| h3-router                | 0.8.6   | ✓      | 66472.8    | 14.55        | 10.90         |
| h3                       | 0.8.6   | ✗      | 66418.4    | 14.57        | 10.89         |
| restana                  | 4.9.9   | ✓      | 62335.2    | 15.55        | 11.12         |
| bare                     | 10.13.0 | ✗      | 60088.8    | 16.14        | 10.72         |
| foxify                   | 0.10.20 | ✓      | 58912.8    | 16.47        | 9.66          |
| polka                    | 0.5.2   | ✓      | 58528.0    | 16.59        | 10.44         |
| connect                  | 3.7.0   | ✗      | 56094.4    | 17.32        | 10.00         |
| server-base              | 7.1.32  | ✗      | 55344.8    | 17.57        | 9.87          |
| fastify                  | 4.29.1  | ✓      | 55220.8    | 17.61        | 9.90          |
| micro                    | 9.4.1   | ✗      | 54904.8    | 17.72        | 9.79          |
| server-base-router       | 7.1.32  | ✓      | 54785.6    | 17.75        | 9.77          |
| yeps                     | 1.1.1   | ✗      | 51690.4    | 18.85        | 9.22          |
| connect-router           | 1.3.8   | ✓      | 50250.4    | 19.40        | 8.96          |
| micro-route              | 2.5.0   | ✓      | 49545.6    | 19.68        | 8.84          |
| trek-engine              | 1.0.5   | ✗      | 48395.2    | 20.17        | 7.94          |
| trek-router              | 1.2.0   | ✓      | 47480.8    | 20.56        | 7.79          |
| vapr                     | 0.6.0   | ✓      | 45208.8    | 21.62        | 7.42          |
| spirit                   | 0.6.1   | ✗      | 44975.2    | 21.76        | 8.02          |
| spirit-router            | 0.5.0   | ✓      | 43364.0    | 22.56        | 7.73          |
| yeps-router              | 1.2.0   | ✓      | 43107.2    | 22.70        | 7.69          |
| koa                      | 2.16.1  | ✗      | 41495.2    | 23.60        | 7.40          |
| total.js                 | 3.4.13  | ✓      | 39097.8    | 25.08        | 11.97         |
| restify                  | 8.6.1   | ✓      | 38988.0    | 25.15        | 7.03          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38499.8    | 25.47        | 6.87          |
| take-five                | 2.0.0   | ✓      | 38182.2    | 25.69        | 13.73         |
| koa-router               | 12.0.1  | ✓      | 36355.4    | 27.00        | 6.48          |
| hapi                     | 20.3.0  | ✓      | 33328.4    | 29.51        | 5.94          |
| microrouter              | 3.1.3   | ✓      | 31838.2    | 30.91        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 27150.0    | 36.33        | 6.01          |
| egg.js                   | 3.30.1  | ✓      | 17133.0    | 57.82        | 6.13          |
| express                  | 4.21.2  | ✓      | 13259.6    | 74.87        | 2.36          |
| fastify-big-json         | 4.29.1  | ✓      | 12671.2    | 78.35        | 145.80        |
| express-with-middlewares | 4.21.2  | ✓      | 12286.6    | 80.84        | 4.57          |
| express-route-prefix     | 4.21.2  | ✓      | 10956.6    | 90.70        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

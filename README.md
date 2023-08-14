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

* __Machine:__ linux x64 | 2 vCPUs | 6.8GB Mem
* __Node:__ `v14.21.3`
* __Run:__ Mon Aug 14 2023 02:05:13 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 56011.2    | 17.36        | 9.99          |
| polkadot                 | 1.0.0   | ✗      | 55524.0    | 17.52        | 9.90          |
| polka                    | 0.5.2   | ✓      | 55264.8    | 17.61        | 9.86          |
| foxify                   | 0.10.20 | ✓      | 54364.8    | 17.89        | 8.92          |
| micro                    | 9.4.1   | ✗      | 54362.4    | 17.90        | 9.69          |
| 0http                    | 3.5.2   | ✓      | 54287.2    | 17.94        | 9.68          |
| h3                       | 0.8.6   | ✗      | 53932.0    | 18.06        | 8.85          |
| connect                  | 3.7.0   | ✗      | 53880.6    | 18.06        | 9.61          |
| fastify                  | 4.21.0  | ✓      | 53307.2    | 18.26        | 9.56          |
| server-base              | 7.1.32  | ✗      | 52715.2    | 18.47        | 9.40          |
| h3-router                | 0.8.6   | ✓      | 52519.2    | 18.55        | 8.62          |
| yeps                     | 1.1.1   | ✗      | 51340.0    | 18.98        | 9.16          |
| server-base-router       | 7.1.32  | ✓      | 51175.2    | 19.04        | 9.13          |
| restana                  | 4.9.7   | ✓      | 49240.8    | 19.83        | 8.78          |
| connect-router           | 1.3.8   | ✓      | 48252.0    | 20.23        | 8.60          |
| trek-engine              | 1.0.5   | ✗      | 47061.8    | 20.76        | 7.72          |
| micro-route              | 2.5.0   | ✓      | 46838.4    | 20.85        | 8.35          |
| trek-router              | 1.2.0   | ✓      | 46601.8    | 20.96        | 7.64          |
| vapr                     | 0.6.0   | ✓      | 43108.8    | 22.70        | 7.07          |
| koa                      | 2.14.2  | ✗      | 40552.8    | 24.16        | 7.23          |
| spirit                   | 0.6.1   | ✗      | 39133.6    | 25.06        | 6.98          |
| yeps-router              | 1.2.0   | ✓      | 38980.8    | 25.16        | 6.95          |
| spirit-router            | 0.5.0   | ✓      | 37329.4    | 26.30        | 6.66          |
| total.js                 | 3.4.13  | ✓      | 37151.8    | 26.42        | 11.37         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37012.2    | 26.51        | 6.60          |
| take-five                | 2.0.0   | ✓      | 36964.6    | 26.56        | 13.29         |
| restify                  | 8.6.1   | ✓      | 35251.0    | 27.86        | 6.35          |
| koa-router               | 12.0.0  | ✓      | 34588.6    | 28.42        | 6.17          |
| hapi                     | 20.3.0  | ✓      | 30335.6    | 32.47        | 5.41          |
| microrouter              | 3.1.3   | ✓      | 28666.0    | 34.38        | 5.11          |
| trpc-router              | 9.27.3  | ✓      | 24802.4    | 39.82        | 5.49          |
| egg.js                   | 3.17.4  | ✓      | 14681.0    | 67.60        | 5.25          |
| express                  | 4.18.2  | ✓      | 11878.8    | 83.61        | 2.12          |
| express-with-middlewares | 4.18.2  | ✓      | 10462.4    | 95.00        | 3.89          |
| express-route-prefix     | 4.18.2  | ✓      | 10273.2    | 96.80        | 3.80          |
| fastify-big-json         | 4.21.0  | ✓      | 9751.5     | 102.09       | 112.20        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

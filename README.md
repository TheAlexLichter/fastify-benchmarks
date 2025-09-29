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
* __Run:__ Mon Sep 29 2025 02:48:43 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 65895.6    | 14.68        | 11.75         |
| h3                       | 0.8.6   | ✗      | 65813.2    | 14.70        | 10.80         |
| 0http                    | 3.5.3   | ✓      | 64902.0    | 14.91        | 11.57         |
| h3-router                | 0.8.6   | ✓      | 64694.0    | 14.95        | 10.61         |
| restana                  | 4.9.9   | ✓      | 60725.6    | 15.97        | 10.83         |
| foxify                   | 0.10.20 | ✓      | 59857.6    | 16.21        | 9.82          |
| bare                     | 10.13.0 | ✗      | 59477.6    | 16.31        | 10.61         |
| polka                    | 0.5.2   | ✓      | 57800.0    | 16.81        | 10.31         |
| fastify                  | 4.29.1  | ✓      | 56724.0    | 17.13        | 10.17         |
| connect                  | 3.7.0   | ✗      | 55252.8    | 17.60        | 9.85          |
| server-base              | 7.1.32  | ✗      | 54335.2    | 17.90        | 9.69          |
| micro                    | 9.4.1   | ✗      | 54316.0    | 17.91        | 9.69          |
| server-base-router       | 7.1.32  | ✓      | 53945.6    | 18.04        | 9.62          |
| yeps                     | 1.1.1   | ✗      | 52707.2    | 18.47        | 9.40          |
| connect-router           | 1.3.8   | ✓      | 50658.4    | 19.24        | 9.03          |
| micro-route              | 2.5.0   | ✓      | 50015.2    | 19.50        | 8.92          |
| trek-engine              | 1.0.5   | ✗      | 47685.6    | 20.47        | 7.82          |
| trek-router              | 1.2.0   | ✓      | 47075.2    | 20.74        | 7.72          |
| vapr                     | 0.6.0   | ✓      | 45946.4    | 21.27        | 7.54          |
| yeps-router              | 1.2.0   | ✓      | 44261.6    | 22.10        | 7.89          |
| spirit-router            | 0.5.0   | ✓      | 42625.6    | 22.96        | 7.60          |
| koa                      | 2.16.2  | ✗      | 42072.0    | 23.26        | 7.50          |
| spirit                   | 0.6.1   | ✗      | 40712.0    | 24.07        | 7.26          |
| total.js                 | 3.4.13  | ✓      | 39792.0    | 24.63        | 12.18         |
| take-five                | 2.0.0   | ✓      | 39599.4    | 24.75        | 14.24         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38858.6    | 25.23        | 6.93          |
| restify                  | 8.6.1   | ✓      | 38681.8    | 25.36        | 6.97          |
| koa-router               | 12.0.1  | ✓      | 36083.0    | 27.21        | 6.44          |
| hapi                     | 20.3.0  | ✓      | 33941.4    | 28.96        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 31485.0    | 31.26        | 5.61          |
| trpc-router              | 9.27.4  | ✓      | 27301.6    | 36.12        | 6.04          |
| egg.js                   | 3.31.0  | ✓      | 16732.6    | 59.24        | 5.98          |
| express                  | 4.21.2  | ✓      | 13205.8    | 75.19        | 2.35          |
| fastify-big-json         | 4.29.1  | ✓      | 12463.0    | 79.70        | 143.39        |
| express-with-middlewares | 4.21.2  | ✓      | 12362.6    | 80.34        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 10748.2    | 92.45        | 3.98          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Sep 15 2025 02:52:37 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 62815.2    | 15.43        | 11.20         |
| h3                       | 0.8.6   | ✗      | 62484.0    | 15.49        | 10.25         |
| h3-router                | 0.8.6   | ✓      | 62231.2    | 15.56        | 10.21         |
| 0http                    | 3.5.3   | ✓      | 60960.8    | 15.91        | 10.87         |
| foxify                   | 0.10.20 | ✓      | 59074.4    | 16.43        | 9.69          |
| restana                  | 4.9.9   | ✓      | 58496.0    | 16.60        | 10.43         |
| bare                     | 10.13.0 | ✗      | 57216.0    | 16.98        | 10.20         |
| connect                  | 3.7.0   | ✗      | 55863.2    | 17.40        | 9.96          |
| polka                    | 0.5.2   | ✓      | 54713.6    | 17.78        | 9.76          |
| server-base-router       | 7.1.32  | ✓      | 54492.8    | 17.85        | 9.72          |
| fastify                  | 4.29.1  | ✓      | 52444.8    | 18.57        | 9.40          |
| micro                    | 9.4.1   | ✗      | 52223.2    | 18.65        | 9.31          |
| server-base              | 7.1.32  | ✗      | 51619.2    | 18.87        | 9.21          |
| yeps                     | 1.1.1   | ✗      | 51144.8    | 19.05        | 9.12          |
| connect-router           | 1.3.8   | ✓      | 50844.0    | 19.17        | 9.07          |
| micro-route              | 2.5.0   | ✓      | 48815.2    | 19.99        | 8.71          |
| trek-engine              | 1.0.5   | ✗      | 47243.2    | 20.67        | 7.75          |
| vapr                     | 0.6.0   | ✓      | 45792.8    | 21.33        | 7.51          |
| trek-router              | 1.2.0   | ✓      | 45114.4    | 21.67        | 7.40          |
| spirit                   | 0.6.1   | ✗      | 43394.4    | 22.55        | 7.74          |
| yeps-router              | 1.2.0   | ✓      | 42841.6    | 22.85        | 7.64          |
| koa                      | 2.16.2  | ✗      | 41785.0    | 23.43        | 7.45          |
| spirit-router            | 0.5.0   | ✓      | 39794.4    | 24.63        | 7.10          |
| take-five                | 2.0.0   | ✓      | 38933.4    | 25.19        | 14.00         |
| total.js                 | 3.4.13  | ✓      | 38820.2    | 25.26        | 11.88         |
| restify                  | 8.6.1   | ✓      | 38508.0    | 25.47        | 6.94          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37725.0    | 26.00        | 6.73          |
| koa-router               | 12.0.1  | ✓      | 35479.0    | 27.69        | 6.33          |
| hapi                     | 20.3.0  | ✓      | 32547.8    | 30.22        | 5.80          |
| microrouter              | 3.1.3   | ✓      | 29880.8    | 32.96        | 5.33          |
| trpc-router              | 9.27.4  | ✓      | 27485.2    | 35.87        | 6.08          |
| egg.js                   | 3.31.0  | ✓      | 17858.6    | 55.47        | 6.39          |
| express                  | 4.21.2  | ✓      | 13057.0    | 76.03        | 2.33          |
| fastify-big-json         | 4.29.1  | ✓      | 12486.4    | 79.57        | 143.66        |
| express-with-middlewares | 4.21.2  | ✓      | 12224.0    | 81.25        | 4.55          |
| express-route-prefix     | 4.21.2  | ✓      | 10810.4    | 91.89        | 4.00          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Apr 27 2026 04:41:32 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 72697.2    | 13.26        | 12.97         |
| polkadot                 | 1.0.0   | ✗      | 72262.4    | 13.34        | 12.89         |
| bare                     | 10.13.0 | ✗      | 71913.2    | 13.41        | 12.82         |
| polka                    | 0.5.2   | ✓      | 69786.0    | 13.83        | 12.45         |
| h3                       | 0.8.6   | ✗      | 69361.2    | 13.91        | 11.38         |
| connect                  | 3.7.0   | ✗      | 69179.2    | 13.96        | 12.34         |
| foxify                   | 0.10.20 | ✓      | 67722.0    | 14.27        | 11.11         |
| h3-router                | 0.8.6   | ✓      | 67217.2    | 14.38        | 11.03         |
| restana                  | 4.9.9   | ✓      | 66806.8    | 14.47        | 11.92         |
| fastify                  | 4.29.1  | ✓      | 65800.4    | 14.70        | 11.80         |
| server-base              | 7.1.32  | ✗      | 65149.6    | 14.85        | 11.62         |
| yeps                     | 1.1.1   | ✗      | 64674.0    | 14.96        | 11.54         |
| server-base-router       | 7.1.32  | ✓      | 64525.6    | 15.00        | 11.51         |
| micro                    | 9.4.1   | ✗      | 64510.0    | 15.00        | 11.50         |
| connect-router           | 1.3.8   | ✓      | 63464.4    | 15.26        | 11.32         |
| micro-route              | 2.5.0   | ✓      | 61517.6    | 15.76        | 10.97         |
| vapr                     | 0.6.0   | ✓      | 56734.4    | 17.13        | 9.31          |
| trek-engine              | 1.0.5   | ✗      | 54491.2    | 17.85        | 8.94          |
| trek-router              | 1.2.0   | ✓      | 54265.6    | 17.94        | 8.90          |
| yeps-router              | 1.2.0   | ✓      | 51128.0    | 19.06        | 9.12          |
| take-five                | 2.0.0   | ✓      | 50393.6    | 19.35        | 18.12         |
| total.js                 | 3.4.13  | ✓      | 49044.0    | 19.90        | 15.01         |
| koa                      | 2.16.4  | ✗      | 48936.0    | 19.94        | 8.73          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 45999.2    | 21.24        | 8.20          |
| restify                  | 8.6.1   | ✓      | 43774.4    | 22.34        | 7.89          |
| spirit                   | 0.6.1   | ✗      | 43324.0    | 22.58        | 7.73          |
| koa-router               | 12.0.1  | ✓      | 42763.2    | 22.89        | 7.63          |
| spirit-router            | 0.5.0   | ✓      | 41167.2    | 23.78        | 7.34          |
| microrouter              | 3.1.3   | ✓      | 39913.6    | 24.55        | 7.12          |
| hapi                     | 20.3.0  | ✓      | 36604.2    | 26.82        | 6.53          |
| trpc-router              | 9.27.4  | ✓      | 31217.4    | 31.53        | 6.91          |
| egg.js                   | 3.34.0  | ✓      | 19015.2    | 52.06        | 6.80          |
| express                  | 4.22.1  | ✓      | 16378.9    | 60.53        | 2.92          |
| express-with-middlewares | 4.22.1  | ✓      | 15067.0    | 65.83        | 5.60          |
| fastify-big-json         | 4.29.1  | ✓      | 12579.8    | 78.94        | 144.74        |
| express-route-prefix     | 4.22.1  | ✓      | 12111.4    | 81.97        | 4.48          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

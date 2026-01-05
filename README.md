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
* __Run:__ Mon Jan 05 2026 03:22:23 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66255.2    | 14.60        | 11.82         |
| polkadot                 | 1.0.0   | ✗      | 64621.6    | 14.97        | 11.52         |
| h3                       | 0.8.6   | ✗      | 61973.6    | 15.64        | 10.17         |
| bare                     | 10.13.0 | ✗      | 59288.8    | 16.37        | 10.57         |
| h3-router                | 0.8.6   | ✓      | 58992.0    | 16.45        | 9.68          |
| restana                  | 4.9.9   | ✓      | 58911.2    | 16.47        | 10.51         |
| polka                    | 0.5.2   | ✓      | 57232.0    | 16.97        | 10.21         |
| connect                  | 3.7.0   | ✗      | 56657.6    | 17.15        | 10.10         |
| foxify                   | 0.10.20 | ✓      | 56390.4    | 17.23        | 9.25          |
| micro                    | 9.4.1   | ✗      | 55474.4    | 17.53        | 9.89          |
| fastify                  | 4.29.1  | ✓      | 55208.0    | 17.61        | 9.90          |
| server-base-router       | 7.1.32  | ✓      | 53827.2    | 18.08        | 9.60          |
| server-base              | 7.1.32  | ✗      | 52530.4    | 18.54        | 9.37          |
| yeps                     | 1.1.1   | ✗      | 51541.6    | 18.91        | 9.19          |
| connect-router           | 1.3.8   | ✓      | 50457.6    | 19.32        | 9.00          |
| micro-route              | 2.5.0   | ✓      | 49256.0    | 19.80        | 8.78          |
| trek-engine              | 1.0.5   | ✗      | 46950.4    | 20.80        | 7.70          |
| trek-router              | 1.2.0   | ✓      | 46396.8    | 21.05        | 7.61          |
| vapr                     | 0.6.0   | ✓      | 46201.6    | 21.14        | 7.58          |
| spirit                   | 0.6.1   | ✗      | 42692.8    | 22.92        | 7.61          |
| yeps-router              | 1.2.0   | ✓      | 42326.4    | 23.13        | 7.55          |
| koa                      | 2.16.3  | ✗      | 39990.2    | 24.50        | 7.13          |
| spirit-router            | 0.5.0   | ✓      | 39972.0    | 24.53        | 7.13          |
| total.js                 | 3.4.13  | ✓      | 38957.6    | 25.17        | 11.93         |
| restify                  | 8.6.1   | ✓      | 38149.0    | 25.71        | 6.88          |
| take-five                | 2.0.0   | ✓      | 37682.2    | 26.04        | 13.55         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37257.8    | 26.34        | 6.64          |
| koa-router               | 12.0.1  | ✓      | 35605.8    | 27.59        | 6.35          |
| hapi                     | 20.3.0  | ✓      | 31540.4    | 31.20        | 5.62          |
| microrouter              | 3.1.3   | ✓      | 31112.4    | 31.63        | 5.55          |
| trpc-router              | 9.27.4  | ✓      | 26294.8    | 37.52        | 5.82          |
| egg.js                   | 3.32.0  | ✓      | 16500.7    | 60.08        | 5.90          |
| express                  | 4.22.1  | ✓      | 13170.8    | 75.36        | 2.35          |
| fastify-big-json         | 4.29.1  | ✓      | 12396.8    | 80.13        | 142.64        |
| express-with-middlewares | 4.22.1  | ✓      | 12119.4    | 81.96        | 4.51          |
| express-route-prefix     | 4.22.1  | ✓      | 10604.1    | 93.73        | 3.92          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

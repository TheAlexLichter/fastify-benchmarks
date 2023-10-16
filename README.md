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
* __Run:__ Mon Oct 16 2023 02:08:59 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 57547.2    | 16.90        | 10.26         |
| foxify                   | 0.10.20 | ✓      | 56354.4    | 17.24        | 9.24          |
| polka                    | 0.5.2   | ✓      | 55804.0    | 17.42        | 9.95          |
| bare                     | 10.13.0 | ✗      | 55587.2    | 17.50        | 9.91          |
| connect                  | 3.7.0   | ✗      | 54605.6    | 17.83        | 9.74          |
| micro                    | 9.4.1   | ✗      | 54293.6    | 17.92        | 9.68          |
| 0http                    | 3.5.2   | ✓      | 53874.4    | 18.05        | 9.61          |
| fastify                  | 4.24.2  | ✓      | 53859.2    | 18.08        | 9.66          |
| h3                       | 0.8.6   | ✗      | 53683.2    | 18.14        | 8.81          |
| h3-router                | 0.8.6   | ✓      | 52884.8    | 18.42        | 8.68          |
| server-base              | 7.1.32  | ✗      | 51704.8    | 18.85        | 9.22          |
| yeps                     | 1.1.1   | ✗      | 50086.4    | 19.47        | 8.93          |
| server-base-router       | 7.1.32  | ✓      | 49380.8    | 19.76        | 8.81          |
| connect-router           | 1.3.8   | ✓      | 48760.0    | 20.01        | 8.70          |
| restana                  | 4.9.7   | ✓      | 48636.8    | 20.08        | 8.67          |
| micro-route              | 2.5.0   | ✓      | 47661.6    | 20.49        | 8.50          |
| vapr                     | 0.6.0   | ✓      | 44101.6    | 22.18        | 7.23          |
| trek-router              | 1.2.0   | ✓      | 44027.0    | 22.22        | 7.22          |
| trek-engine              | 1.0.5   | ✗      | 43802.6    | 22.34        | 7.19          |
| yeps-router              | 1.2.0   | ✓      | 40818.4    | 24.00        | 7.28          |
| koa                      | 2.14.2  | ✗      | 40156.8    | 24.41        | 7.16          |
| spirit                   | 0.6.1   | ✗      | 38771.2    | 25.30        | 6.91          |
| spirit-router            | 0.5.0   | ✓      | 37612.0    | 26.10        | 6.71          |
| take-five                | 2.0.0   | ✓      | 37143.4    | 26.43        | 13.35         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36983.0    | 26.54        | 6.60          |
| total.js                 | 3.4.13  | ✓      | 36964.6    | 26.56        | 11.32         |
| restify                  | 8.6.1   | ✓      | 35237.2    | 27.90        | 6.35          |
| koa-router               | 12.0.1  | ✓      | 34599.2    | 28.42        | 6.17          |
| hapi                     | 20.3.0  | ✓      | 30700.0    | 32.08        | 5.47          |
| microrouter              | 3.1.3   | ✓      | 28779.6    | 34.25        | 5.13          |
| trpc-router              | 9.27.3  | ✓      | 23777.6    | 41.55        | 5.26          |
| egg.js                   | 3.17.5  | ✓      | 14313.4    | 69.33        | 5.12          |
| express                  | 4.18.2  | ✓      | 11880.6    | 83.63        | 2.12          |
| express-with-middlewares | 4.18.2  | ✓      | 10199.5    | 97.48        | 3.79          |
| fastify-big-json         | 4.24.2  | ✓      | 9702.0     | 102.69       | 111.62        |
| express-route-prefix     | 4.18.2  | ✓      | 8291.2     | 119.95       | 3.07          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

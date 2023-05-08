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
* __Run:__ Mon May 08 2023 02:25:12 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polka                    | 0.5.2   | ✓      | 49198.4    | 19.83        | 8.77          |
| foxify                   | 0.10.20 | ✓      | 49107.2    | 19.87        | 8.05          |
| polkadot                 | 1.0.0   | ✗      | 48394.4    | 20.17        | 8.63          |
| bare                     | 10.13.0 | ✗      | 48308.0    | 20.20        | 8.62          |
| fastify                  | 4.17.0  | ✓      | 47629.6    | 20.49        | 8.54          |
| micro                    | 9.4.1   | ✗      | 47296.8    | 20.65        | 8.43          |
| server-base              | 7.1.32  | ✗      | 46249.6    | 21.12        | 8.25          |
| server-base-router       | 7.1.32  | ✓      | 45820.0    | 21.33        | 8.17          |
| 0http                    | 3.5.2   | ✓      | 45770.4    | 21.35        | 8.16          |
| connect                  | 3.7.0   | ✗      | 45531.2    | 21.47        | 8.12          |
| h3-router                | 0.8.6   | ✓      | 45254.4    | 21.61        | 7.42          |
| h3                       | 0.8.6   | ✗      | 44720.8    | 21.87        | 7.34          |
| yeps                     | 1.1.1   | ✗      | 44320.8    | 22.06        | 7.90          |
| connect-router           | 1.3.8   | ✓      | 43155.2    | 22.67        | 7.70          |
| restana                  | 4.9.7   | ✓      | 42456.0    | 23.07        | 7.57          |
| micro-route              | 2.5.0   | ✓      | 42032.6    | 23.29        | 7.50          |
| trek-engine              | 1.0.5   | ✗      | 39267.4    | 24.97        | 6.44          |
| vapr                     | 0.6.0   | ✓      | 38332.2    | 25.59        | 6.29          |
| trek-router              | 1.2.0   | ✓      | 38137.8    | 25.72        | 6.26          |
| yeps-router              | 1.2.0   | ✓      | 36027.8    | 27.26        | 6.42          |
| koa                      | 2.14.2  | ✗      | 35312.2    | 27.82        | 6.30          |
| spirit                   | 0.6.1   | ✗      | 34632.0    | 28.40        | 6.18          |
| spirit-router            | 0.5.0   | ✓      | 32904.0    | 29.93        | 5.87          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 32495.6    | 30.27        | 5.80          |
| take-five                | 2.0.0   | ✓      | 32029.6    | 30.72        | 11.52         |
| restify                  | 8.6.1   | ✓      | 31884.6    | 30.86        | 5.75          |
| total.js                 | 3.4.13  | ✓      | 31377.6    | 31.36        | 9.61          |
| koa-router               | 12.0.0  | ✓      | 29610.4    | 33.27        | 5.28          |
| hapi                     | 20.3.0  | ✓      | 25646.0    | 38.48        | 4.57          |
| microrouter              | 3.1.3   | ✓      | 25392.8    | 38.87        | 4.53          |
| trpc-router              | 9.27.3  | ✓      | 21613.2    | 45.77        | 4.78          |
| egg.js                   | 3.15.0  | ✓      | 12891.2    | 77.03        | 4.61          |
| express                  | 4.18.2  | ✓      | 10584.6    | 93.89        | 1.89          |
| fastify-big-json         | 4.17.0  | ✓      | 9056.9     | 109.93       | 104.21        |
| express-with-middlewares | 4.18.2  | ✓      | 9008.9     | 110.41       | 3.35          |
| express-route-prefix     | 4.18.2  | ✓      | 8814.0     | 112.91       | 3.26          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

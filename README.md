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
* __Node:__ `v14.21.1`
* __Run:__ Mon Nov 28 2022 02:42:08 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 57906.4    | 16.77        | 10.33         |
| foxify                   | 0.10.20 | ✓      | 55515.2    | 17.52        | 9.11          |
| 0http                    | 3.4.1   | ✓      | 55435.2    | 17.54        | 9.89          |
| polkadot                 | 1.0.0   | ✗      | 55234.4    | 17.61        | 9.85          |
| micro                    | 9.4.1   | ✗      | 55148.8    | 17.64        | 9.84          |
| connect                  | 3.7.0   | ✗      | 54586.4    | 17.82        | 9.74          |
| h3-router                | 0.8.6   | ✓      | 54235.2    | 17.94        | 8.90          |
| h3                       | 0.8.6   | ✗      | 54071.2    | 18.00        | 8.87          |
| fastify                  | 4.10.2  | ✓      | 53958.4    | 18.03        | 9.67          |
| polka                    | 0.5.2   | ✓      | 53872.0    | 18.07        | 9.61          |
| server-base              | 7.1.32  | ✗      | 53487.2    | 18.22        | 9.54          |
| server-base-router       | 7.1.32  | ✓      | 53347.2    | 18.25        | 9.51          |
| yeps                     | 1.1.1   | ✗      | 51427.2    | 18.95        | 9.17          |
| connect-router           | 1.3.7   | ✓      | 49929.6    | 19.53        | 8.90          |
| restana                  | 4.9.6   | ✓      | 49842.4    | 19.57        | 8.89          |
| micro-route              | 2.5.0   | ✓      | 47628.8    | 20.50        | 8.49          |
| trek-engine              | 1.0.5   | ✗      | 45667.0    | 21.42        | 7.49          |
| trek-router              | 1.2.0   | ✓      | 45538.2    | 21.46        | 7.47          |
| vapr                     | 0.6.0   | ✓      | 43844.0    | 22.31        | 7.19          |
| yeps-router              | 1.2.0   | ✓      | 41182.4    | 23.78        | 7.34          |
| koa                      | 2.13.4  | ✗      | 38944.6    | 25.18        | 6.95          |
| spirit                   | 0.6.1   | ✗      | 38435.2    | 25.52        | 6.85          |
| spirit-router            | 0.5.0   | ✓      | 37422.4    | 26.23        | 6.67          |
| restify                  | 8.6.1   | ✓      | 37204.6    | 26.38        | 6.71          |
| take-five                | 2.0.0   | ✓      | 37059.4    | 26.48        | 13.32         |
| total.js                 | 3.4.13  | ✓      | 37049.0    | 26.49        | 11.34         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37004.6    | 26.54        | 6.60          |
| koa-router               | 12.0.0  | ✓      | 33117.2    | 29.70        | 5.91          |
| hapi                     | 20.2.2  | ✓      | 29981.2    | 32.85        | 5.35          |
| microrouter              | 3.1.3   | ✓      | 29113.6    | 33.84        | 5.19          |
| trpc-router              | 9.27.4  | ✓      | 24818.0    | 39.78        | 5.49          |
| egg.js                   | 3.5.0   | ✓      | 18790.3    | 52.72        | 6.72          |
| express                  | 4.18.2  | ✓      | 12345.2    | 80.46        | 2.20          |
| express-with-middlewares | 4.18.2  | ✓      | 10695.5    | 92.92        | 3.98          |
| express-route-prefix     | 4.18.2  | ✓      | 10393.2    | 95.65        | 3.85          |
| fastify-big-json         | 4.10.2  | ✓      | 10114.9    | 98.31        | 116.37        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

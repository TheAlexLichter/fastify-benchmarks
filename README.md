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
* __Run:__ Mon Jul 06 2026 05:09:45 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 80492.8    | 11.94        | 14.35         |
| bare                     | 10.13.0 | ✗      | 76582.0    | 12.56        | 13.66         |
| connect                  | 3.7.0   | ✗      | 76409.6    | 12.59        | 13.63         |
| polkadot                 | 1.0.0   | ✗      | 75902.4    | 12.67        | 13.54         |
| polka                    | 0.5.2   | ✓      | 75081.2    | 12.82        | 13.39         |
| restana                  | 4.9.9   | ✓      | 73371.6    | 13.14        | 13.08         |
| h3                       | 0.8.6   | ✗      | 72378.8    | 13.32        | 11.87         |
| server-base-router       | 7.1.32  | ✓      | 71100.4    | 13.57        | 12.68         |
| micro                    | 9.4.1   | ✗      | 70462.8    | 13.70        | 12.57         |
| h3-router                | 0.8.6   | ✓      | 70346.8    | 13.72        | 11.54         |
| server-base              | 7.1.32  | ✗      | 69903.6    | 13.81        | 12.47         |
| foxify                   | 0.10.20 | ✓      | 69778.0    | 13.83        | 11.45         |
| fastify                  | 4.29.1  | ✓      | 69708.4    | 13.85        | 12.50         |
| micro-route              | 2.5.0   | ✓      | 65746.8    | 14.72        | 11.72         |
| connect-router           | 1.3.8   | ✓      | 65338.8    | 14.81        | 11.65         |
| yeps                     | 1.1.1   | ✗      | 65117.2    | 14.86        | 11.61         |
| trek-engine              | 1.0.5   | ✗      | 61877.6    | 15.67        | 10.15         |
| trek-router              | 1.2.0   | ✓      | 61798.4    | 15.68        | 10.14         |
| vapr                     | 0.6.0   | ✓      | 59256.8    | 16.38        | 9.72          |
| yeps-router              | 1.2.0   | ✓      | 55303.2    | 17.59        | 9.86          |
| koa                      | 2.16.4  | ✗      | 53324.8    | 18.25        | 9.51          |
| take-five                | 2.0.0   | ✓      | 51770.4    | 18.82        | 18.61         |
| spirit                   | 0.6.1   | ✗      | 51060.8    | 19.08        | 9.11          |
| total.js                 | 3.4.13  | ✓      | 50382.4    | 19.35        | 15.42         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 49227.2    | 19.82        | 8.78          |
| spirit-router            | 0.5.0   | ✓      | 48908.0    | 19.95        | 8.72          |
| restify                  | 8.6.1   | ✓      | 48829.6    | 19.98        | 8.80          |
| koa-router               | 12.0.1  | ✓      | 45517.6    | 21.47        | 8.12          |
| microrouter              | 3.1.3   | ✓      | 38761.0    | 25.30        | 6.91          |
| hapi                     | 20.3.0  | ✓      | 38676.2    | 25.36        | 6.90          |
| trpc-router              | 9.27.4  | ✓      | 32833.6    | 29.95        | 7.26          |
| egg.js                   | 3.34.0  | ✓      | 18527.5    | 53.46        | 6.63          |
| express                  | 4.22.2  | ✓      | 15702.9    | 63.15        | 2.80          |
| express-with-middlewares | 4.22.2  | ✓      | 14509.6    | 68.38        | 5.40          |
| fastify-big-json         | 4.29.1  | ✓      | 12092.0    | 82.16        | 139.12        |
| express-route-prefix     | 4.22.2  | ✓      | 11649.4    | 85.27        | 4.31          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

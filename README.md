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
* __Run:__ Mon Apr 21 2025 02:54:42 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69470.0    | 13.88        | 12.39         |
| polkadot                 | 1.0.0   | ✗      | 67066.8    | 14.42        | 11.96         |
| h3                       | 0.8.6   | ✗      | 66984.4    | 14.42        | 10.99         |
| h3-router                | 0.8.6   | ✓      | 66476.4    | 14.53        | 10.90         |
| restana                  | 4.9.9   | ✓      | 61178.4    | 15.88        | 10.91         |
| foxify                   | 0.10.20 | ✓      | 60065.6    | 16.15        | 9.85          |
| bare                     | 10.13.0 | ✗      | 59794.4    | 16.21        | 10.66         |
| polka                    | 0.5.2   | ✓      | 57965.6    | 16.74        | 10.34         |
| connect                  | 3.7.0   | ✗      | 56848.0    | 17.09        | 10.14         |
| micro                    | 9.4.1   | ✗      | 56448.8    | 17.22        | 10.07         |
| fastify                  | 4.29.0  | ✓      | 55771.2    | 17.43        | 10.00         |
| server-base-router       | 7.1.32  | ✓      | 55340.0    | 17.56        | 9.87          |
| server-base              | 7.1.32  | ✗      | 54687.2    | 17.78        | 9.75          |
| yeps                     | 1.1.1   | ✗      | 52944.0    | 18.39        | 9.44          |
| connect-router           | 1.3.8   | ✓      | 51462.4    | 18.93        | 9.18          |
| micro-route              | 2.5.0   | ✓      | 50220.0    | 19.40        | 8.96          |
| trek-engine              | 1.0.5   | ✗      | 49623.2    | 19.64        | 8.14          |
| trek-router              | 1.2.0   | ✓      | 49069.6    | 19.89        | 8.05          |
| vapr                     | 0.6.0   | ✓      | 46372.0    | 21.06        | 7.61          |
| spirit                   | 0.6.1   | ✗      | 44823.2    | 21.87        | 7.99          |
| yeps-router              | 1.2.0   | ✓      | 44652.8    | 21.91        | 7.96          |
| spirit-router            | 0.5.0   | ✓      | 43697.6    | 22.34        | 7.79          |
| koa                      | 2.16.1  | ✗      | 42757.6    | 22.89        | 7.63          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40078.4    | 24.45        | 7.15          |
| total.js                 | 3.4.13  | ✓      | 39679.2    | 24.70        | 12.15         |
| take-five                | 2.0.0   | ✓      | 39580.0    | 24.76        | 14.23         |
| restify                  | 8.6.1   | ✓      | 39294.6    | 24.95        | 7.08          |
| koa-router               | 12.0.1  | ✓      | 36775.8    | 26.70        | 6.56          |
| hapi                     | 20.3.0  | ✓      | 33793.2    | 29.09        | 6.03          |
| microrouter              | 3.1.3   | ✓      | 31824.2    | 30.93        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 27586.4    | 35.75        | 6.10          |
| egg.js                   | 3.30.1  | ✓      | 17794.5    | 55.67        | 6.36          |
| express                  | 4.21.2  | ✓      | 13789.2    | 71.97        | 2.46          |
| fastify-big-json         | 4.29.0  | ✓      | 12957.6    | 76.63        | 149.09        |
| express-with-middlewares | 4.21.2  | ✓      | 12471.0    | 79.63        | 4.64          |
| express-route-prefix     | 4.21.2  | ✓      | 11051.4    | 89.88        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

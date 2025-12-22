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
* __Run:__ Mon Dec 22 2025 03:13:32 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67187.6    | 14.39        | 11.98         |
| polkadot                 | 1.0.0   | ✗      | 65928.4    | 14.67        | 11.76         |
| h3                       | 0.8.6   | ✗      | 63302.8    | 15.31        | 10.38         |
| h3-router                | 0.8.6   | ✓      | 62842.4    | 15.41        | 10.31         |
| restana                  | 4.9.9   | ✓      | 61190.4    | 15.87        | 10.91         |
| bare                     | 10.13.0 | ✗      | 61060.0    | 15.89        | 10.89         |
| foxify                   | 0.10.20 | ✓      | 58903.2    | 16.48        | 9.66          |
| polka                    | 0.5.2   | ✓      | 57723.2    | 16.84        | 10.29         |
| connect                  | 3.7.0   | ✗      | 57563.2    | 16.88        | 10.27         |
| micro                    | 9.4.1   | ✗      | 57136.8    | 17.01        | 10.19         |
| fastify                  | 4.29.1  | ✓      | 56730.4    | 17.13        | 10.17         |
| server-base              | 7.1.32  | ✗      | 55472.8    | 17.52        | 9.89          |
| server-base-router       | 7.1.32  | ✓      | 54064.8    | 18.00        | 9.64          |
| yeps                     | 1.1.1   | ✗      | 51905.6    | 18.77        | 9.26          |
| micro-route              | 2.5.0   | ✓      | 48923.2    | 19.94        | 8.72          |
| connect-router           | 1.3.8   | ✓      | 48877.6    | 19.96        | 8.72          |
| trek-engine              | 1.0.5   | ✗      | 46997.6    | 20.78        | 7.71          |
| trek-router              | 1.2.0   | ✓      | 45410.4    | 21.52        | 7.45          |
| vapr                     | 0.6.0   | ✓      | 45033.6    | 21.71        | 7.39          |
| spirit                   | 0.6.1   | ✗      | 44367.2    | 22.05        | 7.91          |
| yeps-router              | 1.2.0   | ✓      | 43260.8    | 22.62        | 7.71          |
| koa                      | 2.16.3  | ✗      | 41967.2    | 23.34        | 7.48          |
| spirit-router            | 0.5.0   | ✓      | 41764.0    | 23.45        | 7.45          |
| total.js                 | 3.4.13  | ✓      | 39427.8    | 24.86        | 12.07         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39243.2    | 24.99        | 7.00          |
| restify                  | 8.6.1   | ✓      | 39226.6    | 24.99        | 7.07          |
| take-five                | 2.0.0   | ✓      | 38236.2    | 25.65        | 13.75         |
| koa-router               | 12.0.1  | ✓      | 36632.2    | 26.79        | 6.53          |
| hapi                     | 20.3.0  | ✓      | 33161.6    | 29.65        | 5.91          |
| microrouter              | 3.1.3   | ✓      | 32100.4    | 30.65        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 27128.0    | 36.35        | 6.00          |
| egg.js                   | 3.31.0  | ✓      | 17272.5    | 57.37        | 6.18          |
| express                  | 4.22.1  | ✓      | 13551.4    | 73.22        | 2.42          |
| fastify-big-json         | 4.29.1  | ✓      | 12777.0    | 77.72        | 147.00        |
| express-with-middlewares | 4.22.1  | ✓      | 12382.2    | 80.21        | 4.61          |
| express-route-prefix     | 4.22.1  | ✓      | 10994.2    | 90.36        | 4.07          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

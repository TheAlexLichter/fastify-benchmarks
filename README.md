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
* __Run:__ Mon May 15 2023 02:28:40 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 57617.6    | 16.87        | 10.28         |
| bare                     | 10.13.0 | ✗      | 57401.6    | 16.93        | 10.24         |
| micro                    | 9.4.1   | ✗      | 56419.2    | 17.23        | 10.06         |
| polka                    | 0.5.2   | ✓      | 56121.6    | 17.33        | 10.01         |
| foxify                   | 0.10.20 | ✓      | 55960.0    | 17.38        | 9.18          |
| fastify                  | 4.17.0  | ✓      | 55690.4    | 17.47        | 9.98          |
| h3                       | 0.8.6   | ✗      | 54582.4    | 17.82        | 8.95          |
| h3-router                | 0.8.6   | ✓      | 54575.2    | 17.82        | 8.95          |
| connect                  | 3.7.0   | ✗      | 54462.4    | 17.87        | 9.71          |
| 0http                    | 3.5.2   | ✓      | 54227.2    | 17.97        | 9.67          |
| server-base-router       | 7.1.32  | ✓      | 53917.6    | 18.05        | 9.62          |
| server-base              | 7.1.32  | ✗      | 52998.4    | 18.37        | 9.45          |
| connect-router           | 1.3.8   | ✓      | 51679.2    | 18.86        | 9.22          |
| yeps                     | 1.1.1   | ✗      | 50314.4    | 19.38        | 8.97          |
| restana                  | 4.9.7   | ✓      | 49794.4    | 19.66        | 8.88          |
| micro-route              | 2.5.0   | ✓      | 47099.2    | 20.74        | 8.40          |
| trek-engine              | 1.0.5   | ✗      | 46594.2    | 20.97        | 7.64          |
| trek-router              | 1.2.0   | ✓      | 44777.4    | 21.83        | 7.35          |
| vapr                     | 0.6.0   | ✓      | 44231.2    | 22.11        | 7.26          |
| yeps-router              | 1.2.0   | ✓      | 40948.8    | 23.93        | 7.30          |
| koa                      | 2.14.2  | ✗      | 40175.0    | 24.41        | 7.16          |
| spirit                   | 0.6.1   | ✗      | 39220.0    | 25.01        | 6.99          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38051.4    | 25.78        | 6.79          |
| take-five                | 2.0.0   | ✓      | 37869.4    | 25.90        | 13.62         |
| total.js                 | 3.4.13  | ✓      | 37410.2    | 26.23        | 11.45         |
| spirit-router            | 0.5.0   | ✓      | 37304.2    | 26.32        | 6.65          |
| restify                  | 8.6.1   | ✓      | 36551.0    | 26.86        | 6.59          |
| koa-router               | 12.0.0  | ✓      | 34758.2    | 28.27        | 6.20          |
| hapi                     | 20.3.0  | ✓      | 30324.0    | 32.48        | 5.41          |
| microrouter              | 3.1.3   | ✓      | 29388.8    | 33.52        | 5.24          |
| trpc-router              | 9.27.3  | ✓      | 24687.2    | 40.02        | 5.46          |
| egg.js                   | 3.16.0  | ✓      | 15245.8    | 65.07        | 5.45          |
| express                  | 4.18.2  | ✓      | 11946.4    | 83.14        | 2.13          |
| fastify-big-json         | 4.17.0  | ✓      | 10579.6    | 94.06        | 121.72        |
| express-route-prefix     | 4.18.2  | ✓      | 10543.9    | 94.24        | 3.90          |
| express-with-middlewares | 4.18.2  | ✓      | 10508.3    | 94.58        | 3.91          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Dec 23 2024 02:40:34 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69714.4    | 13.85        | 12.43         |
| polkadot                 | 1.0.0   | ✗      | 66113.2    | 14.62        | 11.79         |
| h3                       | 0.8.6   | ✗      | 65779.2    | 14.69        | 10.79         |
| h3-router                | 0.8.6   | ✓      | 65574.0    | 14.76        | 10.76         |
| restana                  | 4.9.9   | ✓      | 61729.6    | 15.70        | 11.01         |
| bare                     | 10.13.0 | ✗      | 61429.6    | 15.80        | 10.96         |
| foxify                   | 0.10.20 | ✓      | 60392.8    | 16.06        | 9.91          |
| polka                    | 0.5.2   | ✓      | 60000.8    | 16.16        | 10.70         |
| connect                  | 3.7.0   | ✗      | 57818.4    | 16.79        | 10.31         |
| fastify                  | 4.29.0  | ✓      | 56451.2    | 17.22        | 10.12         |
| server-base-router       | 7.1.32  | ✓      | 55863.2    | 17.40        | 9.96          |
| micro                    | 9.4.1   | ✗      | 55459.2    | 17.53        | 9.89          |
| server-base              | 7.1.32  | ✗      | 54397.6    | 17.88        | 9.70          |
| yeps                     | 1.1.1   | ✗      | 53295.2    | 18.27        | 9.50          |
| connect-router           | 1.3.8   | ✓      | 51110.4    | 19.06        | 9.11          |
| micro-route              | 2.5.0   | ✓      | 50649.6    | 19.25        | 9.03          |
| trek-engine              | 1.0.5   | ✗      | 48642.4    | 20.06        | 7.98          |
| trek-router              | 1.2.0   | ✓      | 48427.2    | 20.16        | 7.94          |
| vapr                     | 0.6.0   | ✓      | 46233.6    | 21.14        | 7.58          |
| yeps-router              | 1.2.0   | ✓      | 44764.0    | 21.83        | 7.98          |
| spirit                   | 0.6.1   | ✗      | 42728.0    | 22.93        | 7.62          |
| koa                      | 2.15.3  | ✗      | 42592.0    | 22.99        | 7.60          |
| spirit-router            | 0.5.0   | ✓      | 41357.6    | 23.67        | 7.38          |
| total.js                 | 3.4.13  | ✓      | 40471.2    | 24.20        | 12.39         |
| restify                  | 8.6.1   | ✓      | 39955.2    | 24.55        | 7.20          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39886.6    | 24.58        | 7.11          |
| take-five                | 2.0.0   | ✓      | 39234.6    | 24.98        | 14.11         |
| koa-router               | 12.0.1  | ✓      | 38408.6    | 25.52        | 6.85          |
| hapi                     | 20.3.0  | ✓      | 33770.8    | 29.10        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 32707.6    | 30.06        | 5.83          |
| trpc-router              | 9.27.4  | ✓      | 27948.4    | 35.27        | 6.18          |
| egg.js                   | 3.29.0  | ✓      | 17743.0    | 55.84        | 6.35          |
| express                  | 4.21.2  | ✓      | 13287.4    | 74.71        | 2.37          |
| fastify-big-json         | 4.29.0  | ✓      | 12873.4    | 77.13        | 148.14        |
| express-with-middlewares | 4.21.2  | ✓      | 12652.4    | 78.48        | 4.71          |
| express-route-prefix     | 4.21.2  | ✓      | 10951.4    | 90.73        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

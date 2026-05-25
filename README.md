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
* __Run:__ Mon May 25 2026 05:32:48 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68579.6    | 14.08        | 12.23         |
| polkadot                 | 1.0.0   | ✗      | 64964.8    | 14.89        | 11.59         |
| h3-router                | 0.8.6   | ✓      | 64337.6    | 15.06        | 10.55         |
| h3                       | 0.8.6   | ✗      | 63428.0    | 15.26        | 10.40         |
| restana                  | 4.9.9   | ✓      | 61290.4    | 15.81        | 10.93         |
| bare                     | 10.13.0 | ✗      | 60304.8    | 16.09        | 10.75         |
| foxify                   | 0.10.20 | ✓      | 59640.8    | 16.26        | 9.78          |
| connect                  | 3.7.0   | ✗      | 58752.0    | 16.51        | 10.48         |
| polka                    | 0.5.2   | ✓      | 57858.4    | 16.79        | 10.32         |
| micro                    | 9.4.1   | ✗      | 57432.8    | 16.91        | 10.24         |
| fastify                  | 4.29.1  | ✓      | 56572.0    | 17.18        | 10.14         |
| server-base              | 7.1.32  | ✗      | 56291.2    | 17.27        | 10.04         |
| server-base-router       | 7.1.32  | ✓      | 55600.8    | 17.49        | 9.92          |
| yeps                     | 1.1.1   | ✗      | 53618.4    | 18.16        | 9.56          |
| connect-router           | 1.3.8   | ✓      | 51064.8    | 19.09        | 9.11          |
| trek-engine              | 1.0.5   | ✗      | 50062.4    | 19.48        | 8.21          |
| micro-route              | 2.5.0   | ✓      | 49456.0    | 19.73        | 8.82          |
| trek-router              | 1.2.0   | ✓      | 48436.6    | 20.15        | 7.94          |
| vapr                     | 0.6.0   | ✓      | 46511.2    | 21.01        | 7.63          |
| spirit                   | 0.6.1   | ✗      | 45785.6    | 21.32        | 8.16          |
| spirit-router            | 0.5.0   | ✓      | 43484.8    | 22.50        | 7.75          |
| yeps-router              | 1.2.0   | ✓      | 43473.6    | 22.50        | 7.75          |
| koa                      | 2.16.4  | ✗      | 42285.6    | 23.14        | 7.54          |
| total.js                 | 3.4.13  | ✓      | 40221.4    | 24.36        | 12.31         |
| take-five                | 2.0.0   | ✓      | 39249.8    | 24.98        | 14.11         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38773.0    | 25.29        | 6.91          |
| restify                  | 8.6.1   | ✓      | 38494.2    | 25.48        | 6.94          |
| koa-router               | 12.0.1  | ✓      | 35824.2    | 27.41        | 6.39          |
| hapi                     | 20.3.0  | ✓      | 33403.2    | 29.44        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 32219.2    | 30.53        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 27658.8    | 35.65        | 6.12          |
| egg.js                   | 3.34.0  | ✓      | 16868.2    | 58.76        | 6.03          |
| express                  | 4.22.2  | ✓      | 13464.8    | 73.72        | 2.40          |
| fastify-big-json         | 4.29.1  | ✓      | 12452.4    | 79.76        | 143.27        |
| express-with-middlewares | 4.22.2  | ✓      | 11911.6    | 83.41        | 4.43          |
| express-route-prefix     | 4.22.2  | ✓      | 10450.4    | 95.10        | 3.87          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

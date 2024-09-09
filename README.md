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
* __Run:__ Mon Sep 09 2024 02:35:10 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69961.2    | 13.80        | 12.48         |
| polkadot                 | 1.0.0   | ✗      | 67735.6    | 14.27        | 12.08         |
| h3                       | 0.8.6   | ✗      | 63170.0    | 15.34        | 10.36         |
| h3-router                | 0.8.6   | ✓      | 63052.4    | 15.36        | 10.34         |
| bare                     | 10.13.0 | ✗      | 62011.2    | 15.65        | 11.06         |
| foxify                   | 0.10.20 | ✓      | 60488.8    | 16.03        | 9.92          |
| restana                  | 4.9.9   | ✓      | 60381.6    | 16.07        | 10.77         |
| polka                    | 0.5.2   | ✓      | 58524.0    | 16.59        | 10.44         |
| connect                  | 3.7.0   | ✗      | 57385.6    | 16.93        | 10.23         |
| server-base              | 7.1.32  | ✗      | 57132.8    | 17.01        | 10.19         |
| micro                    | 9.4.1   | ✗      | 56421.6    | 17.23        | 10.06         |
| fastify                  | 4.28.1  | ✓      | 56107.2    | 17.33        | 10.06         |
| server-base-router       | 7.1.32  | ✓      | 55155.2    | 17.62        | 9.84          |
| yeps                     | 1.1.1   | ✗      | 52479.2    | 18.56        | 9.36          |
| connect-router           | 1.3.8   | ✓      | 51780.0    | 18.82        | 9.23          |
| micro-route              | 2.5.0   | ✓      | 51132.8    | 19.06        | 9.12          |
| trek-engine              | 1.0.5   | ✗      | 49061.6    | 19.89        | 8.05          |
| trek-router              | 1.2.0   | ✓      | 48029.6    | 20.32        | 7.88          |
| vapr                     | 0.6.0   | ✓      | 45981.6    | 21.25        | 7.54          |
| yeps-router              | 1.2.0   | ✓      | 44738.4    | 21.85        | 7.98          |
| spirit                   | 0.6.1   | ✗      | 44488.8    | 22.01        | 7.93          |
| spirit-router            | 0.5.0   | ✓      | 43136.0    | 22.67        | 7.69          |
| koa                      | 2.15.3  | ✗      | 42918.4    | 22.79        | 7.65          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40401.4    | 24.25        | 7.20          |
| take-five                | 2.0.0   | ✓      | 39838.2    | 24.60        | 14.32         |
| total.js                 | 3.4.13  | ✓      | 39516.0    | 24.81        | 12.10         |
| restify                  | 8.6.1   | ✓      | 39328.6    | 24.92        | 7.09          |
| koa-router               | 12.0.1  | ✓      | 37465.0    | 26.19        | 6.68          |
| hapi                     | 20.3.0  | ✓      | 34112.8    | 28.82        | 6.08          |
| microrouter              | 3.1.3   | ✓      | 32356.0    | 30.39        | 5.77          |
| trpc-router              | 9.27.4  | ✓      | 27144.8    | 36.34        | 6.01          |
| egg.js                   | 3.27.1  | ✓      | 17655.6    | 56.10        | 6.31          |
| express                  | 4.19.2  | ✓      | 13699.8    | 72.46        | 2.44          |
| fastify-big-json         | 4.28.1  | ✓      | 12828.0    | 77.40        | 147.59        |
| express-with-middlewares | 4.19.2  | ✓      | 12524.4    | 79.29        | 4.66          |
| express-route-prefix     | 4.19.2  | ✓      | 11111.8    | 89.41        | 4.11          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

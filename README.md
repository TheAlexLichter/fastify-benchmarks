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
* __Run:__ Mon Sep 08 2025 02:51:19 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66931.2    | 14.44        | 11.94         |
| polkadot                 | 1.0.0   | ✗      | 64132.0    | 15.10        | 11.44         |
| h3                       | 0.8.6   | ✗      | 60080.8    | 16.16        | 9.86          |
| h3-router                | 0.8.6   | ✓      | 60056.0    | 16.15        | 9.85          |
| bare                     | 10.13.0 | ✗      | 59316.8    | 16.36        | 10.58         |
| restana                  | 4.9.9   | ✓      | 58521.6    | 16.58        | 10.44         |
| foxify                   | 0.10.20 | ✓      | 56866.4    | 17.09        | 9.33          |
| polka                    | 0.5.2   | ✓      | 56238.4    | 17.29        | 10.03         |
| connect                  | 3.7.0   | ✗      | 55147.2    | 17.64        | 9.83          |
| server-base-router       | 7.1.32  | ✓      | 55050.4    | 17.66        | 9.82          |
| micro                    | 9.4.1   | ✗      | 54411.2    | 17.88        | 9.70          |
| fastify                  | 4.29.1  | ✓      | 53570.4    | 18.17        | 9.60          |
| server-base              | 7.1.32  | ✗      | 52308.0    | 18.62        | 9.33          |
| yeps                     | 1.1.1   | ✗      | 50560.8    | 19.28        | 9.02          |
| connect-router           | 1.3.8   | ✓      | 48828.8    | 19.98        | 8.71          |
| micro-route              | 2.5.0   | ✓      | 48643.2    | 20.07        | 8.68          |
| trek-engine              | 1.0.5   | ✗      | 45437.6    | 21.51        | 7.45          |
| vapr                     | 0.6.0   | ✓      | 43974.4    | 22.25        | 7.21          |
| trek-router              | 1.2.0   | ✓      | 43669.8    | 22.40        | 7.16          |
| yeps-router              | 1.2.0   | ✓      | 42768.0    | 22.88        | 7.63          |
| spirit                   | 0.6.1   | ✗      | 40737.6    | 24.06        | 7.27          |
| spirit-router            | 0.5.0   | ✓      | 39538.4    | 24.78        | 7.05          |
| koa                      | 2.16.2  | ✗      | 39513.6    | 24.81        | 7.05          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38459.0    | 25.50        | 6.86          |
| take-five                | 2.0.0   | ✓      | 38458.2    | 25.50        | 13.83         |
| restify                  | 8.6.1   | ✓      | 37945.8    | 25.85        | 6.84          |
| total.js                 | 3.4.13  | ✓      | 37543.0    | 26.13        | 11.49         |
| koa-router               | 12.0.1  | ✓      | 34930.6    | 28.13        | 6.23          |
| hapi                     | 20.3.0  | ✓      | 32450.6    | 30.31        | 5.79          |
| microrouter              | 3.1.3   | ✓      | 30834.4    | 31.93        | 5.50          |
| trpc-router              | 9.27.4  | ✓      | 26554.0    | 37.15        | 5.88          |
| egg.js                   | 3.31.0  | ✓      | 16511.2    | 60.03        | 5.90          |
| express                  | 4.21.2  | ✓      | 13130.0    | 75.60        | 2.34          |
| fastify-big-json         | 4.29.1  | ✓      | 12381.4    | 80.21        | 142.45        |
| express-with-middlewares | 4.21.2  | ✓      | 12265.8    | 80.98        | 4.56          |
| express-route-prefix     | 4.21.2  | ✓      | 10654.5    | 93.27        | 3.94          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Feb 12 2024 02:06:34 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68396.4    | 14.12        | 12.20         |
| h3                       | 0.8.6   | ✗      | 67217.6    | 14.38        | 11.03         |
| h3-router                | 0.8.6   | ✓      | 64926.4    | 14.91        | 10.65         |
| 0http                    | 3.5.2   | ✓      | 64143.2    | 15.09        | 11.44         |
| bare                     | 10.13.0 | ✗      | 60532.8    | 16.01        | 10.80         |
| foxify                   | 0.10.20 | ✓      | 59133.6    | 16.41        | 9.70          |
| polka                    | 0.5.2   | ✓      | 58890.4    | 16.49        | 10.50         |
| restana                  | 4.9.7   | ✓      | 56321.6    | 17.27        | 10.04         |
| connect                  | 3.7.0   | ✗      | 56104.8    | 17.31        | 10.00         |
| micro                    | 9.4.1   | ✗      | 56072.8    | 17.34        | 10.00         |
| server-base              | 7.1.32  | ✗      | 55452.0    | 17.55        | 9.89          |
| fastify                  | 4.26.0  | ✓      | 55100.8    | 17.65        | 9.88          |
| server-base-router       | 7.1.32  | ✓      | 54428.8    | 17.87        | 9.71          |
| yeps                     | 1.1.1   | ✗      | 52133.6    | 18.69        | 9.30          |
| connect-router           | 1.3.8   | ✓      | 50418.4    | 19.32        | 8.99          |
| micro-route              | 2.5.0   | ✓      | 50376.0    | 19.35        | 8.98          |
| trek-router              | 1.2.0   | ✓      | 48532.8    | 20.10        | 7.96          |
| trek-engine              | 1.0.5   | ✗      | 48364.8    | 20.18        | 7.93          |
| vapr                     | 0.6.0   | ✓      | 46494.4    | 21.01        | 7.63          |
| yeps-router              | 1.2.0   | ✓      | 44612.8    | 21.94        | 7.96          |
| spirit                   | 0.6.1   | ✗      | 44383.2    | 22.11        | 7.92          |
| koa                      | 2.15.0  | ✗      | 42708.0    | 22.92        | 7.62          |
| spirit-router            | 0.5.0   | ✓      | 42224.0    | 23.18        | 7.53          |
| total.js                 | 3.4.13  | ✓      | 39605.6    | 24.76        | 12.12         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39588.6    | 24.76        | 7.06          |
| restify                  | 8.6.1   | ✓      | 39426.2    | 24.86        | 7.11          |
| take-five                | 2.0.0   | ✓      | 39109.4    | 25.08        | 14.06         |
| koa-router               | 12.0.1  | ✓      | 37400.6    | 26.24        | 6.67          |
| hapi                     | 20.3.0  | ✓      | 33899.6    | 29.01        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 32523.6    | 30.24        | 5.80          |
| trpc-router              | 9.27.4  | ✓      | 26932.4    | 36.62        | 5.96          |
| egg.js                   | 3.19.0  | ✓      | 18057.5    | 54.85        | 6.46          |
| express                  | 4.18.2  | ✓      | 13627.4    | 72.84        | 2.43          |
| fastify-big-json         | 4.26.0  | ✓      | 13100.4    | 75.79        | 150.74        |
| express-with-middlewares | 4.18.2  | ✓      | 12513.8    | 79.36        | 4.65          |
| express-route-prefix     | 4.18.2  | ✓      | 11138.2    | 89.22        | 4.12          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

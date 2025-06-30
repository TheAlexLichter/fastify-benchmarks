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
* __Run:__ Mon Jun 30 2025 03:11:20 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69552.8    | 13.87        | 12.40         |
| polkadot                 | 1.0.0   | ✗      | 66783.6    | 14.48        | 11.91         |
| h3-router                | 0.8.6   | ✓      | 64814.0    | 14.93        | 10.63         |
| h3                       | 0.8.6   | ✗      | 63982.4    | 15.14        | 10.49         |
| bare                     | 10.13.0 | ✗      | 61310.4    | 15.83        | 10.93         |
| foxify                   | 0.10.20 | ✓      | 60380.0    | 16.06        | 9.90          |
| restana                  | 4.9.9   | ✓      | 60119.2    | 16.16        | 10.72         |
| polka                    | 0.5.2   | ✓      | 57757.6    | 16.83        | 10.30         |
| connect                  | 3.7.0   | ✗      | 57226.4    | 16.98        | 10.21         |
| fastify                  | 4.29.1  | ✓      | 56004.8    | 17.36        | 10.04         |
| micro                    | 9.4.1   | ✗      | 55572.0    | 17.49        | 9.91          |
| server-base-router       | 7.1.32  | ✓      | 54992.0    | 17.68        | 9.81          |
| server-base              | 7.1.32  | ✗      | 54829.6    | 17.74        | 9.78          |
| yeps                     | 1.1.1   | ✗      | 53368.0    | 18.24        | 9.52          |
| connect-router           | 1.3.8   | ✓      | 50882.4    | 19.16        | 9.07          |
| micro-route              | 2.5.0   | ✓      | 50480.0    | 19.31        | 9.00          |
| trek-engine              | 1.0.5   | ✗      | 48856.0    | 19.97        | 8.01          |
| trek-router              | 1.2.0   | ✓      | 47717.6    | 20.46        | 7.83          |
| vapr                     | 0.6.0   | ✓      | 45978.4    | 21.25        | 7.54          |
| spirit                   | 0.6.1   | ✗      | 45031.2    | 21.75        | 8.03          |
| yeps-router              | 1.2.0   | ✓      | 44289.6    | 22.09        | 7.90          |
| spirit-router            | 0.5.0   | ✓      | 43830.4    | 22.30        | 7.82          |
| koa                      | 2.16.1  | ✗      | 42042.4    | 23.29        | 7.50          |
| total.js                 | 3.4.13  | ✓      | 39216.0    | 25.00        | 12.00         |
| restify                  | 8.6.1   | ✓      | 38966.6    | 25.15        | 7.02          |
| take-five                | 2.0.0   | ✓      | 38662.2    | 25.36        | 13.90         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38450.6    | 25.51        | 6.86          |
| koa-router               | 12.0.1  | ✓      | 36552.2    | 26.86        | 6.52          |
| hapi                     | 20.3.0  | ✓      | 33889.6    | 29.00        | 6.04          |
| microrouter              | 3.1.3   | ✓      | 31334.4    | 31.41        | 5.59          |
| trpc-router              | 9.27.4  | ✓      | 27478.4    | 35.88        | 6.08          |
| egg.js                   | 3.30.1  | ✓      | 17765.2    | 55.77        | 6.35          |
| express                  | 4.21.2  | ✓      | 13678.4    | 72.53        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12697.2    | 78.21        | 146.09        |
| express-with-middlewares | 4.21.2  | ✓      | 12517.2    | 79.33        | 4.66          |
| express-route-prefix     | 4.21.2  | ✓      | 10973.2    | 90.56        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

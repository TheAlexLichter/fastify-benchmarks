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
* __Run:__ Mon Apr 07 2025 02:50:31 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69797.2    | 13.83        | 12.45         |
| polkadot                 | 1.0.0   | ✗      | 67818.0    | 14.25        | 12.10         |
| h3                       | 0.8.6   | ✗      | 66741.2    | 14.48        | 10.95         |
| h3-router                | 0.8.6   | ✓      | 65428.0    | 14.80        | 10.73         |
| restana                  | 4.9.9   | ✓      | 61960.8    | 15.64        | 11.05         |
| bare                     | 10.13.0 | ✗      | 60674.4    | 15.99        | 10.82         |
| foxify                   | 0.10.20 | ✓      | 58697.6    | 16.54        | 9.63          |
| polka                    | 0.5.2   | ✓      | 58233.6    | 16.68        | 10.39         |
| micro                    | 9.4.1   | ✗      | 57369.6    | 16.94        | 10.23         |
| connect                  | 3.7.0   | ✗      | 55826.4    | 17.41        | 9.96          |
| fastify                  | 4.29.0  | ✓      | 55544.8    | 17.51        | 9.96          |
| server-base              | 7.1.32  | ✗      | 54331.2    | 17.91        | 9.69          |
| server-base-router       | 7.1.32  | ✓      | 54228.8    | 17.94        | 9.67          |
| yeps                     | 1.1.1   | ✗      | 53265.6    | 18.28        | 9.50          |
| connect-router           | 1.3.8   | ✓      | 50800.8    | 19.19        | 9.06          |
| micro-route              | 2.5.0   | ✓      | 50439.2    | 19.33        | 8.99          |
| trek-engine              | 1.0.5   | ✗      | 49292.0    | 19.78        | 8.09          |
| trek-router              | 1.2.0   | ✓      | 48935.2    | 19.95        | 8.03          |
| vapr                     | 0.6.0   | ✓      | 46143.2    | 21.17        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 44362.4    | 22.04        | 7.91          |
| yeps-router              | 1.2.0   | ✓      | 43828.0    | 22.31        | 7.82          |
| spirit-router            | 0.5.0   | ✓      | 43223.2    | 22.63        | 7.71          |
| koa                      | 2.16.1  | ✗      | 43072.0    | 22.72        | 7.68          |
| total.js                 | 3.4.13  | ✓      | 39660.8    | 24.72        | 12.14         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39407.0    | 24.88        | 7.03          |
| restify                  | 8.6.1   | ✓      | 39031.2    | 25.12        | 7.04          |
| take-five                | 2.0.0   | ✓      | 38964.6    | 25.17        | 14.01         |
| koa-router               | 12.0.1  | ✓      | 37050.6    | 26.49        | 6.61          |
| hapi                     | 20.3.0  | ✓      | 33938.6    | 28.96        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 32437.0    | 30.32        | 5.78          |
| trpc-router              | 9.27.4  | ✓      | 27668.4    | 35.64        | 6.12          |
| egg.js                   | 3.30.1  | ✓      | 17707.4    | 55.94        | 6.33          |
| express                  | 4.21.2  | ✓      | 13619.0    | 72.85        | 2.43          |
| fastify-big-json         | 4.29.0  | ✓      | 12679.0    | 78.32        | 145.87        |
| express-with-middlewares | 4.21.2  | ✓      | 12374.4    | 80.23        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 10896.2    | 91.18        | 4.03          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

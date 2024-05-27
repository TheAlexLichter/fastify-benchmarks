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
* __Run:__ Mon May 27 2024 02:14:49 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68454.8    | 14.11        | 12.21         |
| polkadot                 | 1.0.0   | ✗      | 67684.0    | 14.28        | 12.07         |
| h3                       | 0.8.6   | ✗      | 63684.0    | 15.22        | 10.45         |
| h3-router                | 0.8.6   | ✓      | 61190.4    | 15.85        | 10.04         |
| bare                     | 10.13.0 | ✗      | 59681.6    | 16.25        | 10.64         |
| foxify                   | 0.10.20 | ✓      | 58564.0    | 16.58        | 9.61          |
| restana                  | 4.9.9   | ✓      | 58394.4    | 16.64        | 10.41         |
| polka                    | 0.5.2   | ✓      | 58268.8    | 16.66        | 10.39         |
| connect                  | 3.7.0   | ✗      | 55601.6    | 17.50        | 9.92          |
| micro                    | 9.4.1   | ✗      | 55253.6    | 17.60        | 9.85          |
| server-base-router       | 7.1.32  | ✓      | 54484.0    | 17.86        | 9.72          |
| fastify                  | 4.27.0  | ✓      | 54106.4    | 17.99        | 9.70          |
| server-base              | 7.1.32  | ✗      | 53302.4    | 18.26        | 9.51          |
| yeps                     | 1.1.1   | ✗      | 52763.2    | 18.46        | 9.41          |
| connect-router           | 1.3.8   | ✓      | 49873.6    | 19.55        | 8.89          |
| micro-route              | 2.5.0   | ✓      | 48949.6    | 19.93        | 8.73          |
| trek-router              | 1.2.0   | ✓      | 46985.4    | 20.78        | 7.71          |
| trek-engine              | 1.0.5   | ✗      | 46776.0    | 20.88        | 7.67          |
| vapr                     | 0.6.0   | ✓      | 44561.6    | 21.94        | 7.31          |
| yeps-router              | 1.2.0   | ✓      | 43765.6    | 22.35        | 7.81          |
| koa                      | 2.15.3  | ✗      | 42150.4    | 23.22        | 7.52          |
| spirit                   | 0.6.1   | ✗      | 41547.2    | 23.57        | 7.41          |
| spirit-router            | 0.5.0   | ✓      | 40920.0    | 23.93        | 7.30          |
| take-five                | 2.0.0   | ✓      | 38849.0    | 25.24        | 13.97         |
| total.js                 | 3.4.13  | ✓      | 38495.4    | 25.48        | 11.78         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38389.4    | 25.55        | 6.85          |
| restify                  | 8.6.1   | ✓      | 38350.2    | 25.58        | 6.91          |
| koa-router               | 12.0.1  | ✓      | 35962.0    | 27.31        | 6.41          |
| hapi                     | 20.3.0  | ✓      | 32510.4    | 30.25        | 5.80          |
| microrouter              | 3.1.3   | ✓      | 31318.6    | 31.42        | 5.59          |
| trpc-router              | 9.27.4  | ✓      | 26453.6    | 37.29        | 5.85          |
| egg.js                   | 3.23.0  | ✓      | 16948.0    | 58.48        | 6.06          |
| express                  | 4.19.2  | ✓      | 13339.4    | 74.40        | 2.38          |
| fastify-big-json         | 4.27.0  | ✓      | 12635.2    | 78.59        | 145.37        |
| express-with-middlewares | 4.19.2  | ✓      | 12322.8    | 80.60        | 4.58          |
| express-route-prefix     | 4.19.2  | ✓      | 10998.8    | 90.34        | 4.07          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

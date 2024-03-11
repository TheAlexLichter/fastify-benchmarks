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
* __Run:__ Mon Mar 11 2024 02:06:52 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 66923.6    | 14.46        | 11.93         |
| h3-router                | 0.8.6   | ✓      | 63983.2    | 15.13        | 10.49         |
| h3                       | 0.8.6   | ✗      | 62804.0    | 15.43        | 10.30         |
| 0http                    | 3.5.2   | ✓      | 61989.6    | 15.64        | 11.05         |
| bare                     | 10.13.0 | ✗      | 59194.4    | 16.40        | 10.56         |
| foxify                   | 0.10.20 | ✓      | 59165.6    | 16.40        | 9.71          |
| restana                  | 4.9.7   | ✓      | 57173.6    | 16.99        | 10.20         |
| polka                    | 0.5.2   | ✓      | 56328.8    | 17.25        | 10.04         |
| connect                  | 3.7.0   | ✗      | 55967.2    | 17.37        | 9.98          |
| micro                    | 9.4.1   | ✗      | 55684.0    | 17.46        | 9.93          |
| fastify                  | 4.26.2  | ✓      | 55180.0    | 17.63        | 9.89          |
| server-base              | 7.1.32  | ✗      | 53979.2    | 18.04        | 9.63          |
| server-base-router       | 7.1.32  | ✓      | 52674.4    | 18.48        | 9.39          |
| yeps                     | 1.1.1   | ✗      | 52418.4    | 18.58        | 9.35          |
| connect-router           | 1.3.8   | ✓      | 50300.0    | 19.38        | 8.97          |
| micro-route              | 2.5.0   | ✓      | 49928.0    | 19.53        | 8.90          |
| trek-engine              | 1.0.5   | ✗      | 48546.4    | 20.10        | 7.96          |
| trek-router              | 1.2.0   | ✓      | 48271.2    | 20.22        | 7.92          |
| vapr                     | 0.6.0   | ✓      | 46990.4    | 20.78        | 7.71          |
| yeps-router              | 1.2.0   | ✓      | 44252.0    | 22.11        | 7.89          |
| spirit                   | 0.6.1   | ✗      | 43973.6    | 22.27        | 7.84          |
| koa                      | 2.15.0  | ✗      | 43241.6    | 22.64        | 7.71          |
| spirit-router            | 0.5.0   | ✓      | 42173.6    | 23.22        | 7.52          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39669.4    | 24.71        | 7.07          |
| total.js                 | 3.4.13  | ✓      | 39343.2    | 24.92        | 12.04         |
| restify                  | 8.6.1   | ✓      | 39292.6    | 24.94        | 7.08          |
| take-five                | 2.0.0   | ✓      | 38779.4    | 25.29        | 13.94         |
| koa-router               | 12.0.1  | ✓      | 36601.8    | 26.82        | 6.53          |
| hapi                     | 20.3.0  | ✓      | 33679.6    | 29.19        | 6.01          |
| microrouter              | 3.1.3   | ✓      | 32096.8    | 30.65        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 26739.6    | 36.89        | 5.92          |
| egg.js                   | 3.20.0  | ✓      | 17341.7    | 57.14        | 6.20          |
| express                  | 4.18.3  | ✓      | 13738.6    | 72.25        | 2.45          |
| fastify-big-json         | 4.26.2  | ✓      | 12770.6    | 77.77        | 146.93        |
| express-with-middlewares | 4.18.3  | ✓      | 12569.4    | 79.01        | 4.67          |
| express-route-prefix     | 4.18.3  | ✓      | 11058.6    | 89.85        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

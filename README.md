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
* __Run:__ Mon Jul 08 2024 02:25:57 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66759.2    | 14.48        | 11.91         |
| h3-router                | 0.8.6   | ✓      | 65155.2    | 14.85        | 10.69         |
| polkadot                 | 1.0.0   | ✗      | 65124.8    | 14.85        | 11.61         |
| h3                       | 0.8.6   | ✗      | 64281.2    | 15.05        | 10.54         |
| restana                  | 4.9.9   | ✓      | 60953.6    | 15.91        | 10.87         |
| foxify                   | 0.10.20 | ✓      | 58756.0    | 16.52        | 9.64          |
| polka                    | 0.5.2   | ✓      | 58410.4    | 16.61        | 10.42         |
| bare                     | 10.13.0 | ✗      | 58362.4    | 16.66        | 10.41         |
| micro                    | 9.4.1   | ✗      | 56692.8    | 17.15        | 10.11         |
| connect                  | 3.7.0   | ✗      | 56589.6    | 17.18        | 10.09         |
| fastify                  | 4.28.1  | ✓      | 54672.0    | 17.79        | 9.80          |
| server-base              | 7.1.32  | ✗      | 54544.0    | 17.84        | 9.73          |
| server-base-router       | 7.1.32  | ✓      | 53930.4    | 18.05        | 9.62          |
| yeps                     | 1.1.1   | ✗      | 53051.2    | 18.35        | 9.46          |
| connect-router           | 1.3.8   | ✓      | 50513.6    | 19.31        | 9.01          |
| micro-route              | 2.5.0   | ✓      | 50231.2    | 19.41        | 8.96          |
| trek-engine              | 1.0.5   | ✗      | 48739.2    | 20.01        | 7.99          |
| trek-router              | 1.2.0   | ✓      | 47330.6    | 20.63        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 45984.8    | 21.25        | 7.54          |
| spirit                   | 0.6.1   | ✗      | 43601.6    | 22.40        | 7.78          |
| yeps-router              | 1.2.0   | ✓      | 43489.6    | 22.49        | 7.76          |
| koa                      | 2.15.3  | ✗      | 42451.2    | 23.07        | 7.57          |
| spirit-router            | 0.5.0   | ✓      | 42386.4    | 23.11        | 7.56          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40013.6    | 24.50        | 7.14          |
| take-five                | 2.0.0   | ✓      | 39018.2    | 25.14        | 14.03         |
| total.js                 | 3.4.13  | ✓      | 38253.4    | 25.64        | 11.71         |
| restify                  | 8.6.1   | ✓      | 38235.8    | 25.65        | 6.89          |
| koa-router               | 12.0.1  | ✓      | 37540.2    | 26.14        | 6.69          |
| hapi                     | 20.3.0  | ✓      | 33447.6    | 29.39        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 30976.4    | 31.77        | 5.52          |
| trpc-router              | 9.27.4  | ✓      | 26194.0    | 37.67        | 5.80          |
| egg.js                   | 3.26.1  | ✓      | 17699.6    | 55.98        | 6.33          |
| express                  | 4.19.2  | ✓      | 13705.2    | 72.40        | 2.44          |
| fastify-big-json         | 4.28.1  | ✓      | 12700.2    | 78.20        | 146.12        |
| express-with-middlewares | 4.19.2  | ✓      | 12453.2    | 79.74        | 4.63          |
| express-route-prefix     | 4.19.2  | ✓      | 10775.0    | 92.21        | 3.99          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

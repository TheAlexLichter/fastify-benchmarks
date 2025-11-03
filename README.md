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
* __Run:__ Mon Nov 03 2025 02:58:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68600.4    | 14.08        | 12.23         |
| polkadot                 | 1.0.0   | ✗      | 65048.4    | 14.87        | 11.60         |
| h3                       | 0.8.6   | ✗      | 64496.4    | 15.01        | 10.58         |
| h3-router                | 0.8.6   | ✓      | 60921.6    | 15.92        | 9.99          |
| bare                     | 10.13.0 | ✗      | 60273.6    | 16.09        | 10.75         |
| foxify                   | 0.10.20 | ✓      | 59937.6    | 16.19        | 9.83          |
| restana                  | 4.9.9   | ✓      | 59684.8    | 16.27        | 10.64         |
| polka                    | 0.5.2   | ✓      | 59190.4    | 16.39        | 10.56         |
| connect                  | 3.7.0   | ✗      | 57293.6    | 16.96        | 10.22         |
| micro                    | 9.4.1   | ✗      | 57231.2    | 16.97        | 10.21         |
| fastify                  | 4.29.1  | ✓      | 56157.6    | 17.31        | 10.07         |
| server-base-router       | 7.1.32  | ✓      | 55608.0    | 17.49        | 9.92          |
| server-base              | 7.1.32  | ✗      | 53472.8    | 18.21        | 9.54          |
| yeps                     | 1.1.1   | ✗      | 52759.2    | 18.45        | 9.41          |
| connect-router           | 1.3.8   | ✓      | 50176.8    | 19.44        | 8.95          |
| micro-route              | 2.5.0   | ✓      | 49501.6    | 19.70        | 8.83          |
| trek-engine              | 1.0.5   | ✗      | 46940.0    | 20.81        | 7.70          |
| trek-router              | 1.2.0   | ✓      | 46631.2    | 20.95        | 7.65          |
| vapr                     | 0.6.0   | ✓      | 45231.2    | 21.61        | 7.42          |
| yeps-router              | 1.2.0   | ✓      | 43359.2    | 22.57        | 7.73          |
| spirit                   | 0.6.1   | ✗      | 42379.2    | 23.10        | 7.56          |
| spirit-router            | 0.5.0   | ✓      | 41671.2    | 23.49        | 7.43          |
| koa                      | 2.16.3  | ✗      | 41291.4    | 23.72        | 7.36          |
| total.js                 | 3.4.13  | ✓      | 39280.0    | 24.96        | 12.03         |
| restify                  | 8.6.1   | ✓      | 38561.8    | 25.44        | 6.95          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38438.2    | 25.52        | 6.86          |
| take-five                | 2.0.0   | ✓      | 37757.8    | 25.98        | 13.58         |
| koa-router               | 12.0.1  | ✓      | 35406.6    | 27.74        | 6.31          |
| hapi                     | 20.3.0  | ✓      | 32036.8    | 30.71        | 5.71          |
| microrouter              | 3.1.3   | ✓      | 31022.4    | 31.73        | 5.53          |
| trpc-router              | 9.27.4  | ✓      | 26570.0    | 37.13        | 5.88          |
| egg.js                   | 3.31.0  | ✓      | 16693.5    | 59.38        | 5.97          |
| express                  | 4.21.2  | ✓      | 13474.6    | 73.67        | 2.40          |
| fastify-big-json         | 4.29.1  | ✓      | 12510.4    | 79.40        | 143.94        |
| express-with-middlewares | 4.21.2  | ✓      | 12327.0    | 80.55        | 4.58          |
| express-route-prefix     | 4.21.2  | ✓      | 10951.8    | 90.74        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

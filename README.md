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
* __Run:__ Mon Sep 30 2024 02:41:17 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69680.4    | 13.84        | 12.43         |
| polkadot                 | 1.0.0   | ✗      | 68780.4    | 14.05        | 12.26         |
| h3                       | 0.8.6   | ✗      | 64514.4    | 15.01        | 10.58         |
| h3-router                | 0.8.6   | ✓      | 63957.2    | 15.14        | 10.49         |
| restana                  | 4.9.9   | ✓      | 60992.8    | 15.91        | 10.88         |
| bare                     | 10.13.0 | ✗      | 59352.0    | 16.35        | 10.59         |
| polka                    | 0.5.2   | ✓      | 57964.8    | 16.76        | 10.34         |
| foxify                   | 0.10.20 | ✓      | 56538.4    | 17.19        | 9.27          |
| connect                  | 3.7.0   | ✗      | 55506.4    | 17.52        | 9.90          |
| micro                    | 9.4.1   | ✗      | 54585.6    | 17.82        | 9.73          |
| fastify                  | 4.28.1  | ✓      | 54137.6    | 17.97        | 9.71          |
| server-base-router       | 7.1.32  | ✓      | 53349.6    | 18.25        | 9.51          |
| server-base              | 7.1.32  | ✗      | 52616.8    | 18.52        | 9.38          |
| yeps                     | 1.1.1   | ✗      | 51575.2    | 18.90        | 9.20          |
| connect-router           | 1.3.8   | ✓      | 49027.2    | 19.91        | 8.74          |
| micro-route              | 2.5.0   | ✓      | 48612.8    | 20.08        | 8.67          |
| trek-router              | 1.2.0   | ✓      | 47188.0    | 20.70        | 7.74          |
| trek-engine              | 1.0.5   | ✗      | 46579.2    | 20.97        | 7.64          |
| vapr                     | 0.6.0   | ✓      | 45502.4    | 21.48        | 7.46          |
| spirit-router            | 0.5.0   | ✓      | 43901.6    | 22.25        | 7.83          |
| spirit                   | 0.6.1   | ✗      | 43298.4    | 22.59        | 7.72          |
| yeps-router              | 1.2.0   | ✓      | 43153.6    | 22.67        | 7.70          |
| koa                      | 2.15.3  | ✗      | 41152.8    | 23.80        | 7.34          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39467.4    | 24.83        | 7.04          |
| restify                  | 8.6.1   | ✓      | 39161.4    | 25.04        | 7.06          |
| take-five                | 2.0.0   | ✓      | 38847.4    | 25.24        | 13.97         |
| total.js                 | 3.4.13  | ✓      | 38516.0    | 25.47        | 11.79         |
| koa-router               | 12.0.1  | ✓      | 36482.2    | 26.91        | 6.51          |
| hapi                     | 20.3.0  | ✓      | 32714.0    | 30.06        | 5.83          |
| microrouter              | 3.1.3   | ✓      | 31375.6    | 31.37        | 5.60          |
| trpc-router              | 9.27.4  | ✓      | 26248.4    | 37.59        | 5.81          |
| egg.js                   | 3.28.0  | ✓      | 17042.9    | 58.14        | 6.09          |
| express                  | 4.21.0  | ✓      | 13994.2    | 70.92        | 2.50          |
| fastify-big-json         | 4.28.1  | ✓      | 12536.6    | 79.21        | 144.23        |
| express-with-middlewares | 4.21.0  | ✓      | 12415.8    | 79.99        | 4.62          |
| express-route-prefix     | 4.21.0  | ✓      | 10774.4    | 92.23        | 3.99          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

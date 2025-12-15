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
* __Run:__ Mon Dec 15 2025 03:11:55 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69156.8    | 13.96        | 12.33         |
| h3                       | 0.8.6   | ✗      | 64558.8    | 14.99        | 10.59         |
| bare                     | 10.13.0 | ✗      | 59494.4    | 16.30        | 10.61         |
| polkadot                 | 1.0.0   | ✗      | 59153.6    | 16.41        | 10.55         |
| h3-router                | 0.8.6   | ✓      | 58873.6    | 16.49        | 9.66          |
| foxify                   | 0.10.20 | ✓      | 57312.0    | 16.95        | 9.40          |
| connect                  | 3.7.0   | ✗      | 56912.8    | 17.08        | 10.15         |
| restana                  | 4.9.9   | ✓      | 56355.2    | 17.26        | 10.05         |
| fastify                  | 4.29.1  | ✓      | 55117.6    | 17.64        | 9.88          |
| server-base-router       | 7.1.32  | ✓      | 53009.6    | 18.37        | 9.45          |
| polka                    | 0.5.2   | ✓      | 52788.0    | 18.44        | 9.41          |
| server-base              | 7.1.32  | ✗      | 52536.0    | 18.54        | 9.37          |
| micro                    | 9.4.1   | ✗      | 52055.2    | 18.71        | 9.28          |
| yeps                     | 1.1.1   | ✗      | 50804.0    | 19.19        | 9.06          |
| connect-router           | 1.3.8   | ✓      | 49716.0    | 19.62        | 8.87          |
| micro-route              | 2.5.0   | ✓      | 48143.2    | 20.27        | 8.59          |
| trek-engine              | 1.0.5   | ✗      | 46040.0    | 21.22        | 7.55          |
| trek-router              | 1.2.0   | ✓      | 44966.2    | 21.74        | 7.38          |
| vapr                     | 0.6.0   | ✓      | 43816.8    | 22.33        | 7.19          |
| yeps-router              | 1.2.0   | ✓      | 41766.4    | 23.44        | 7.45          |
| koa                      | 2.16.3  | ✗      | 40200.2    | 24.38        | 7.17          |
| spirit-router            | 0.5.0   | ✓      | 38923.2    | 25.19        | 6.94          |
| spirit                   | 0.6.1   | ✗      | 37719.2    | 26.01        | 6.73          |
| take-five                | 2.0.0   | ✓      | 37187.0    | 26.39        | 13.37         |
| restify                  | 8.6.1   | ✓      | 36988.6    | 26.54        | 6.67          |
| total.js                 | 3.4.13  | ✓      | 36866.2    | 26.62        | 11.29         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36858.6    | 26.63        | 6.57          |
| koa-router               | 12.0.1  | ✓      | 35282.4    | 27.84        | 6.29          |
| hapi                     | 20.3.0  | ✓      | 31812.8    | 30.93        | 5.67          |
| microrouter              | 3.1.3   | ✓      | 29661.2    | 33.21        | 5.29          |
| trpc-router              | 9.27.4  | ✓      | 25445.6    | 38.79        | 5.63          |
| egg.js                   | 3.31.0  | ✓      | 17530.8    | 56.52        | 6.27          |
| express                  | 4.22.1  | ✓      | 13025.6    | 76.23        | 2.32          |
| fastify-big-json         | 4.29.1  | ✓      | 12657.8    | 78.47        | 145.64        |
| express-with-middlewares | 4.22.1  | ✓      | 12275.6    | 80.90        | 4.57          |
| express-route-prefix     | 4.22.1  | ✓      | 10833.8    | 91.72        | 4.01          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

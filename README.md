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
* __Run:__ Mon Feb 09 2026 03:44:34 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 70542.8    | 13.68        | 12.58         |
| polkadot                 | 1.0.0   | ✗      | 68171.2    | 14.17        | 12.16         |
| h3-router                | 0.8.6   | ✓      | 65716.8    | 14.72        | 10.78         |
| h3                       | 0.8.6   | ✗      | 64804.4    | 14.93        | 10.63         |
| restana                  | 4.9.9   | ✓      | 60070.4    | 16.17        | 10.71         |
| foxify                   | 0.10.20 | ✓      | 59212.0    | 16.39        | 9.71          |
| bare                     | 10.13.0 | ✗      | 58154.4    | 16.70        | 10.37         |
| polka                    | 0.5.2   | ✓      | 57258.4    | 16.96        | 10.21         |
| connect                  | 3.7.0   | ✗      | 56989.6    | 17.06        | 10.16         |
| server-base-router       | 7.1.32  | ✓      | 55981.6    | 17.36        | 9.98          |
| server-base              | 7.1.32  | ✗      | 55283.2    | 17.59        | 9.86          |
| micro                    | 9.4.1   | ✗      | 54688.8    | 17.79        | 9.75          |
| fastify                  | 4.29.1  | ✓      | 54426.4    | 17.87        | 9.76          |
| yeps                     | 1.1.1   | ✗      | 52276.0    | 18.63        | 9.32          |
| connect-router           | 1.3.8   | ✓      | 49995.2    | 19.50        | 8.92          |
| micro-route              | 2.5.0   | ✓      | 49972.0    | 19.52        | 8.91          |
| trek-engine              | 1.0.5   | ✗      | 48039.2    | 20.31        | 7.88          |
| trek-router              | 1.2.0   | ✓      | 46616.8    | 20.95        | 7.65          |
| vapr                     | 0.6.0   | ✓      | 45788.8    | 21.33        | 7.51          |
| spirit                   | 0.6.1   | ✗      | 44325.6    | 22.08        | 7.91          |
| yeps-router              | 1.2.0   | ✓      | 44220.0    | 22.12        | 7.89          |
| spirit-router            | 0.5.0   | ✓      | 43850.4    | 22.29        | 7.82          |
| koa                      | 2.16.3  | ✗      | 41949.6    | 23.34        | 7.48          |
| total.js                 | 3.4.13  | ✓      | 39613.0    | 24.74        | 12.13         |
| take-five                | 2.0.0   | ✓      | 38699.0    | 25.34        | 13.91         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38364.6    | 25.57        | 6.84          |
| restify                  | 8.6.1   | ✓      | 38228.2    | 25.66        | 6.89          |
| koa-router               | 12.0.1  | ✓      | 35927.0    | 27.33        | 6.41          |
| hapi                     | 20.3.0  | ✓      | 33106.6    | 29.71        | 5.90          |
| microrouter              | 3.1.3   | ✓      | 31482.8    | 31.26        | 5.61          |
| trpc-router              | 9.27.4  | ✓      | 26974.4    | 36.57        | 5.97          |
| egg.js                   | 3.34.0  | ✓      | 17434.0    | 56.84        | 6.24          |
| express                  | 4.22.1  | ✓      | 13234.2    | 75.02        | 2.36          |
| fastify-big-json         | 4.29.1  | ✓      | 12448.0    | 79.77        | 143.21        |
| express-with-middlewares | 4.22.1  | ✓      | 12202.8    | 81.38        | 4.54          |
| express-route-prefix     | 4.22.1  | ✓      | 10926.1    | 90.96        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

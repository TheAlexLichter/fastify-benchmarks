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

* __Machine:__ linux x64 | 2 vCPUs | 6.8GB Mem
* __Node:__ `v14.21.3`
* __Run:__ Mon Sep 04 2023 02:06:53 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 49753.6    | 19.61        | 8.87          |
| polkadot                 | 1.0.0   | ✗      | 49676.0    | 19.64        | 8.86          |
| polka                    | 0.5.2   | ✓      | 48992.0    | 19.91        | 8.74          |
| connect                  | 3.7.0   | ✗      | 48969.0    | 19.94        | 8.73          |
| foxify                   | 0.10.20 | ✓      | 48684.0    | 20.04        | 7.99          |
| micro                    | 9.4.1   | ✗      | 47911.2    | 20.37        | 8.54          |
| h3                       | 0.8.6   | ✗      | 47568.8    | 20.54        | 7.80          |
| 0http                    | 3.5.2   | ✓      | 47439.2    | 20.59        | 8.46          |
| h3-router                | 0.8.6   | ✓      | 46899.2    | 20.84        | 7.69          |
| server-base-router       | 7.1.32  | ✓      | 46480.8    | 21.02        | 8.29          |
| fastify                  | 4.22.2  | ✓      | 45777.6    | 21.34        | 8.21          |
| server-base              | 7.1.32  | ✗      | 45238.4    | 21.61        | 8.07          |
| connect-router           | 1.3.8   | ✓      | 43405.6    | 22.54        | 7.74          |
| micro-route              | 2.5.0   | ✓      | 42988.6    | 22.76        | 7.67          |
| restana                  | 4.9.7   | ✓      | 42652.8    | 22.95        | 7.61          |
| yeps                     | 1.1.1   | ✗      | 41340.8    | 23.69        | 7.37          |
| trek-engine              | 1.0.5   | ✗      | 38749.0    | 25.32        | 6.36          |
| trek-router              | 1.2.0   | ✓      | 38725.0    | 25.33        | 6.35          |
| vapr                     | 0.6.0   | ✓      | 38629.0    | 25.39        | 6.34          |
| yeps-router              | 1.2.0   | ✓      | 36191.8    | 27.14        | 6.45          |
| koa                      | 2.14.2  | ✗      | 35662.6    | 27.56        | 6.36          |
| spirit                   | 0.6.1   | ✗      | 35053.4    | 28.04        | 6.25          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 33155.0    | 29.66        | 5.91          |
| spirit-router            | 0.5.0   | ✓      | 33141.0    | 29.70        | 5.91          |
| take-five                | 2.0.0   | ✓      | 32720.8    | 30.06        | 11.76         |
| total.js                 | 3.4.13  | ✓      | 31147.6    | 31.60        | 9.54          |
| restify                  | 8.6.1   | ✓      | 30215.2    | 32.59        | 5.45          |
| koa-router               | 12.0.0  | ✓      | 30096.0    | 32.73        | 5.37          |
| hapi                     | 20.3.0  | ✓      | 26442.4    | 37.31        | 4.72          |
| microrouter              | 3.1.3   | ✓      | 25709.6    | 38.41        | 4.58          |
| trpc-router              | 9.27.3  | ✓      | 21642.4    | 45.70        | 4.79          |
| egg.js                   | 3.17.4  | ✓      | 13041.4    | 76.17        | 4.66          |
| express                  | 4.18.2  | ✓      | 10511.0    | 94.59        | 1.87          |
| express-with-middlewares | 4.18.2  | ✓      | 9049.3     | 109.89       | 3.37          |
| fastify-big-json         | 4.22.2  | ✓      | 8425.6     | 118.20       | 96.94         |
| express-route-prefix     | 4.18.2  | ✓      | 8369.4     | 118.72       | 3.10          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

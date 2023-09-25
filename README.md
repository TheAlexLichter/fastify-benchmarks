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
* __Run:__ Mon Sep 25 2023 02:08:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 32357.0    | 30.42        | 5.77          |
| h3-router                | 0.8.6   | ✓      | 31548.4    | 31.21        | 5.17          |
| h3                       | 0.8.6   | ✗      | 30887.6    | 31.89        | 5.07          |
| bare                     | 10.13.0 | ✗      | 30594.8    | 32.20        | 5.46          |
| 0http                    | 3.5.2   | ✓      | 30586.8    | 32.20        | 5.45          |
| foxify                   | 0.10.20 | ✓      | 30564.4    | 32.22        | 5.01          |
| micro                    | 9.4.1   | ✗      | 30282.6    | 32.54        | 5.40          |
| connect                  | 3.7.0   | ✗      | 30221.8    | 32.60        | 5.39          |
| polka                    | 0.5.2   | ✓      | 29624.8    | 33.26        | 5.28          |
| fastify                  | 4.23.2  | ✓      | 29342.4    | 33.59        | 5.26          |
| server-base-router       | 7.1.32  | ✓      | 28866.0    | 34.14        | 5.15          |
| server-base              | 7.1.32  | ✗      | 28175.2    | 34.99        | 5.02          |
| trek-engine              | 1.0.5   | ✗      | 28122.4    | 35.07        | 4.61          |
| spirit                   | 0.6.1   | ✗      | 27521.6    | 35.87        | 4.91          |
| spirit-router            | 0.5.0   | ✓      | 27458.8    | 36.00        | 4.90          |
| restana                  | 4.9.7   | ✓      | 26794.4    | 36.83        | 4.78          |
| connect-router           | 1.3.8   | ✓      | 25446.4    | 38.81        | 4.54          |
| trek-router              | 1.2.0   | ✓      | 25219.2    | 39.17        | 4.14          |
| micro-route              | 2.5.0   | ✓      | 24503.6    | 40.32        | 4.37          |
| yeps                     | 1.1.1   | ✗      | 23931.6    | 41.28        | 4.27          |
| yeps-router              | 1.2.0   | ✓      | 23020.0    | 42.95        | 4.11          |
| restify                  | 8.6.1   | ✓      | 22208.0    | 44.52        | 4.00          |
| koa                      | 2.14.2  | ✗      | 22102.4    | 44.74        | 3.94          |
| vapr                     | 0.6.0   | ✓      | 21887.7    | 45.21        | 3.59          |
| total.js                 | 3.4.13  | ✓      | 20672.9    | 47.86        | 6.33          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20407.6    | 48.51        | 3.64          |
| take-five                | 2.0.0   | ✓      | 19822.5    | 49.92        | 7.13          |
| koa-router               | 12.0.0  | ✓      | 19440.5    | 50.94        | 3.47          |
| hapi                     | 20.3.0  | ✓      | 18807.3    | 52.67        | 3.35          |
| microrouter              | 3.1.3   | ✓      | 16725.9    | 59.27        | 2.98          |
| trpc-router              | 9.27.3  | ✓      | 16721.4    | 59.28        | 3.70          |
| egg.js                   | 3.17.4  | ✓      | 9010.1     | 110.45       | 3.22          |
| express                  | 4.18.2  | ✓      | 7449.5     | 133.59       | 1.33          |
| fastify-big-json         | 4.23.2  | ✓      | 7046.5     | 141.47       | 81.07         |
| express-with-middlewares | 4.18.2  | ✓      | 6607.7     | 150.71       | 2.46          |
| express-route-prefix     | 4.18.2  | ✓      | 6550.7     | 151.91       | 2.42          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Sep 18 2023 02:07:01 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 29831.2    | 33.05        | 5.32          |
| polka                    | 0.5.2   | ✓      | 29040.4    | 33.95        | 5.18          |
| polkadot                 | 1.0.0   | ✗      | 28721.2    | 34.33        | 5.12          |
| h3-router                | 0.8.6   | ✓      | 28646.0    | 34.43        | 4.70          |
| connect                  | 3.7.0   | ✗      | 27832.0    | 35.47        | 4.96          |
| foxify                   | 0.10.20 | ✓      | 27092.8    | 36.46        | 4.44          |
| h3                       | 0.8.6   | ✗      | 27048.4    | 36.49        | 4.44          |
| micro                    | 9.4.1   | ✗      | 27038.8    | 36.54        | 4.82          |
| server-base-router       | 7.1.32  | ✓      | 26440.8    | 37.31        | 4.72          |
| server-base              | 7.1.32  | ✗      | 26197.6    | 37.67        | 4.67          |
| fastify                  | 4.23.2  | ✓      | 25061.2    | 39.41        | 4.49          |
| yeps                     | 1.1.1   | ✗      | 25002.0    | 39.52        | 4.46          |
| 0http                    | 3.5.2   | ✓      | 24966.8    | 39.55        | 4.45          |
| trek-engine              | 1.0.5   | ✗      | 23751.3    | 41.60        | 3.90          |
| micro-route              | 2.5.0   | ✓      | 23517.2    | 42.03        | 4.19          |
| spirit                   | 0.6.1   | ✗      | 23308.8    | 42.48        | 4.16          |
| connect-router           | 1.3.8   | ✓      | 23026.8    | 42.91        | 4.11          |
| trek-router              | 1.2.0   | ✓      | 22777.5    | 43.43        | 3.74          |
| spirit-router            | 0.5.0   | ✓      | 22487.5    | 43.99        | 4.01          |
| yeps-router              | 1.2.0   | ✓      | 21983.2    | 44.97        | 3.92          |
| vapr                     | 0.6.0   | ✓      | 20938.9    | 47.24        | 3.43          |
| restana                  | 4.9.7   | ✓      | 20717.9    | 47.76        | 3.69          |
| koa                      | 2.14.2  | ✗      | 20231.3    | 48.96        | 3.61          |
| restify                  | 8.6.1   | ✓      | 19656.1    | 50.41        | 3.54          |
| take-five                | 2.0.0   | ✓      | 19387.7    | 51.09        | 6.97          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 19102.7    | 51.88        | 3.41          |
| total.js                 | 3.4.13  | ✓      | 18967.1    | 52.21        | 5.81          |
| koa-router               | 12.0.0  | ✓      | 18849.3    | 52.54        | 3.36          |
| hapi                     | 20.3.0  | ✓      | 18387.3    | 53.88        | 3.28          |
| microrouter              | 3.1.3   | ✓      | 15875.4    | 62.47        | 2.83          |
| trpc-router              | 9.27.3  | ✓      | 15845.4    | 62.58        | 3.51          |
| egg.js                   | 3.17.4  | ✓      | 8277.0     | 120.27       | 2.96          |
| express                  | 4.18.2  | ✓      | 7118.7     | 139.81       | 1.27          |
| fastify-big-json         | 4.23.2  | ✓      | 6394.4     | 155.85       | 73.57         |
| express-with-middlewares | 4.18.2  | ✓      | 6098.6     | 163.27       | 2.27          |
| express-route-prefix     | 4.18.2  | ✓      | 6053.3     | 164.53       | 2.24          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

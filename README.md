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
* __Run:__ Mon Sep 07 2026 05:08:58 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| connect                  | 3.7.0   | ✗      | 99171.2    | 9.58         | 17.68         |
| polkadot                 | 1.0.0   | ✗      | 98859.2    | 9.62         | 17.63         |
| 0http                    | 3.5.3   | ✓      | 97262.4    | 9.79         | 17.35         |
| server-base              | 7.1.32  | ✗      | 96539.2    | 9.86         | 17.22         |
| polka                    | 0.5.2   | ✓      | 96532.8    | 9.87         | 17.22         |
| bare                     | 10.13.0 | ✗      | 95692.8    | 9.96         | 17.06         |
| server-base-router       | 7.1.32  | ✓      | 95577.6    | 9.97         | 17.04         |
| restana                  | 4.9.9   | ✓      | 93073.6    | 10.24        | 16.60         |
| fastify                  | 4.29.1  | ✓      | 92864.0    | 10.28        | 16.65         |
| foxify                   | 0.10.20 | ✓      | 92292.8    | 10.34        | 15.14         |
| connect-router           | 1.3.8   | ✓      | 91699.2    | 10.41        | 16.35         |
| yeps                     | 1.1.1   | ✗      | 90678.4    | 10.53        | 16.17         |
| h3-router                | 0.8.6   | ✓      | 90484.8    | 10.56        | 14.84         |
| micro                    | 9.4.1   | ✗      | 90288.0    | 10.58        | 16.10         |
| h3                       | 0.8.6   | ✗      | 88979.2    | 10.75        | 14.60         |
| micro-route              | 2.5.0   | ✓      | 87236.8    | 10.97        | 15.56         |
| trek-router              | 1.2.0   | ✓      | 76238.8    | 12.62        | 12.51         |
| trek-engine              | 1.0.5   | ✗      | 75478.8    | 12.75        | 12.38         |
| vapr                     | 0.6.0   | ✓      | 74811.6    | 12.87        | 12.27         |
| total.js                 | 3.4.13  | ✓      | 70404.4    | 13.71        | 21.55         |
| take-five                | 2.0.0   | ✓      | 69044.0    | 13.99        | 24.82         |
| yeps-router              | 1.2.0   | ✓      | 66565.6    | 14.52        | 11.87         |
| koa                      | 2.16.4  | ✗      | 64938.4    | 14.91        | 11.58         |
| spirit                   | 0.6.1   | ✗      | 62414.4    | 15.53        | 11.13         |
| spirit-router            | 0.5.0   | ✓      | 62240.8    | 15.57        | 11.10         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 59783.2    | 16.24        | 10.66         |
| restify                  | 8.6.1   | ✓      | 57902.4    | 16.77        | 10.44         |
| koa-router               | 12.0.1  | ✓      | 55461.6    | 17.53        | 9.89          |
| hapi                     | 20.3.0  | ✓      | 52103.2    | 18.70        | 9.29          |
| microrouter              | 3.1.3   | ✓      | 50326.4    | 19.37        | 8.97          |
| trpc-router              | 9.27.4  | ✓      | 43000.0    | 22.76        | 9.51          |
| egg.js                   | 3.34.0  | ✓      | 23381.2    | 42.25        | 8.36          |
| express                  | 4.22.2  | ✓      | 20451.3    | 48.38        | 3.65          |
| express-with-middlewares | 4.22.2  | ✓      | 18446.2    | 53.69        | 6.86          |
| fastify-big-json         | 4.29.1  | ✓      | 15151.6    | 65.48        | 174.32        |
| express-route-prefix     | 4.22.2  | ✓      | 13731.0    | 72.28        | 5.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

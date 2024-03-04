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
* __Run:__ Mon Mar 04 2024 02:06:50 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69410.8    | 13.90        | 12.38         |
| 0http                    | 3.5.2   | ✓      | 65628.4    | 14.74        | 11.70         |
| h3                       | 0.8.6   | ✗      | 63980.8    | 15.13        | 10.49         |
| h3-router                | 0.8.6   | ✓      | 62551.2    | 15.48        | 10.26         |
| bare                     | 10.13.0 | ✗      | 60889.6    | 15.92        | 10.86         |
| polka                    | 0.5.2   | ✓      | 59640.8    | 16.27        | 10.64         |
| foxify                   | 0.10.20 | ✓      | 57667.2    | 16.85        | 9.46          |
| connect                  | 3.7.0   | ✗      | 57123.2    | 17.01        | 10.19         |
| fastify                  | 4.26.2  | ✓      | 56594.4    | 17.18        | 10.15         |
| micro                    | 9.4.1   | ✗      | 56330.4    | 17.26        | 10.05         |
| restana                  | 4.9.7   | ✓      | 55884.0    | 17.41        | 9.97          |
| server-base              | 7.1.32  | ✗      | 55853.6    | 17.41        | 9.96          |
| server-base-router       | 7.1.32  | ✓      | 53373.6    | 18.24        | 9.52          |
| yeps                     | 1.1.1   | ✗      | 52355.2    | 18.60        | 9.34          |
| connect-router           | 1.3.8   | ✓      | 50848.8    | 19.18        | 9.07          |
| micro-route              | 2.5.0   | ✓      | 50414.4    | 19.34        | 8.99          |
| trek-engine              | 1.0.5   | ✗      | 49084.8    | 19.88        | 8.05          |
| trek-router              | 1.2.0   | ✓      | 47654.4    | 20.48        | 7.82          |
| vapr                     | 0.6.0   | ✓      | 47056.0    | 20.75        | 7.72          |
| yeps-router              | 1.2.0   | ✓      | 44954.4    | 21.75        | 8.02          |
| spirit                   | 0.6.1   | ✗      | 43980.8    | 22.22        | 7.84          |
| spirit-router            | 0.5.0   | ✓      | 43512.0    | 22.47        | 7.76          |
| koa                      | 2.15.0  | ✗      | 43370.6    | 22.56        | 7.73          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39693.8    | 24.70        | 7.08          |
| restify                  | 8.6.1   | ✓      | 39400.2    | 24.87        | 7.10          |
| total.js                 | 3.4.13  | ✓      | 39382.2    | 24.90        | 12.06         |
| take-five                | 2.0.0   | ✓      | 39360.2    | 24.91        | 14.15         |
| koa-router               | 12.0.1  | ✓      | 37433.0    | 26.22        | 6.68          |
| hapi                     | 20.3.0  | ✓      | 34196.8    | 28.73        | 6.10          |
| microrouter              | 3.1.3   | ✓      | 32783.4    | 29.99        | 5.85          |
| trpc-router              | 9.27.4  | ✓      | 27098.0    | 36.40        | 6.00          |
| egg.js                   | 3.20.0  | ✓      | 17751.2    | 55.80        | 6.35          |
| express                  | 4.18.3  | ✓      | 13568.8    | 73.16        | 2.42          |
| express-with-middlewares | 4.18.3  | ✓      | 12851.4    | 77.26        | 4.78          |
| fastify-big-json         | 4.26.2  | ✓      | 12567.0    | 79.03        | 144.60        |
| express-route-prefix     | 4.18.3  | ✓      | 11047.8    | 89.96        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

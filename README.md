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
* __Run:__ Mon Apr 10 2023 02:19:18 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 48192.0    | 20.28        | 8.59          |
| bare                     | 10.13.0 | ✗      | 47722.2    | 20.46        | 8.51          |
| connect                  | 3.7.0   | ✗      | 47139.2    | 20.71        | 8.41          |
| foxify                   | 0.10.20 | ✓      | 46972.8    | 20.79        | 7.70          |
| polka                    | 0.5.2   | ✓      | 46905.6    | 20.82        | 8.36          |
| 0http                    | 3.5.1   | ✓      | 46280.8    | 21.13        | 8.25          |
| server-base              | 7.1.32  | ✗      | 46239.2    | 21.13        | 8.25          |
| fastify                  | 4.15.0  | ✓      | 46015.2    | 21.23        | 8.25          |
| micro                    | 9.4.1   | ✗      | 45653.6    | 21.41        | 8.14          |
| h3                       | 0.8.6   | ✗      | 45302.4    | 21.58        | 7.43          |
| server-base-router       | 7.1.32  | ✓      | 44722.4    | 21.86        | 7.98          |
| h3-router                | 0.8.6   | ✓      | 44663.8    | 21.90        | 7.33          |
| connect-router           | 1.3.8   | ✓      | 43044.0    | 22.74        | 7.68          |
| yeps                     | 1.1.1   | ✗      | 42848.8    | 22.84        | 7.64          |
| micro-route              | 2.5.0   | ✓      | 42549.4    | 23.01        | 7.59          |
| restana                  | 4.9.7   | ✓      | 42044.6    | 23.29        | 7.50          |
| trek-router              | 1.2.0   | ✓      | 39207.0    | 25.02        | 6.43          |
| trek-engine              | 1.0.5   | ✗      | 39141.4    | 25.07        | 6.42          |
| vapr                     | 0.6.0   | ✓      | 37283.0    | 26.32        | 6.12          |
| yeps-router              | 1.2.0   | ✓      | 36209.4    | 27.12        | 6.46          |
| spirit                   | 0.6.1   | ✗      | 35155.6    | 27.98        | 6.27          |
| koa                      | 2.14.1  | ✗      | 34493.8    | 28.48        | 6.15          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 33810.0    | 29.08        | 6.03          |
| spirit-router            | 0.5.0   | ✓      | 32497.6    | 30.32        | 5.80          |
| take-five                | 2.0.0   | ✓      | 31783.2    | 30.97        | 11.43         |
| total.js                 | 3.4.13  | ✓      | 31587.2    | 31.15        | 9.67          |
| restify                  | 8.6.1   | ✓      | 30791.2    | 31.98        | 5.55          |
| koa-router               | 12.0.0  | ✓      | 29034.0    | 33.94        | 5.18          |
| hapi                     | 20.3.0  | ✓      | 26062.4    | 37.86        | 4.65          |
| microrouter              | 3.1.3   | ✓      | 24788.8    | 39.83        | 4.42          |
| trpc-router              | 9.27.3  | ✓      | 21235.6    | 46.58        | 4.70          |
| egg.js                   | 3.15.0  | ✓      | 12858.4    | 77.25        | 4.60          |
| express                  | 4.18.2  | ✓      | 10570.1    | 94.03        | 1.88          |
| express-with-middlewares | 4.18.2  | ✓      | 9101.3     | 109.27       | 3.38          |
| fastify-big-json         | 4.15.0  | ✓      | 9079.9     | 109.58       | 104.47        |
| express-route-prefix     | 4.18.2  | ✓      | 8925.2     | 111.42       | 3.30          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

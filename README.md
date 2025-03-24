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
* __Run:__ Mon Mar 24 2025 02:49:13 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66356.4    | 14.57        | 11.83         |
| polkadot                 | 1.0.0   | ✗      | 64423.2    | 15.03        | 11.49         |
| h3                       | 0.8.6   | ✗      | 61300.4    | 15.82        | 10.05         |
| h3-router                | 0.8.6   | ✓      | 60959.2    | 15.91        | 10.00         |
| bare                     | 10.13.0 | ✗      | 60944.8    | 15.92        | 10.87         |
| foxify                   | 0.10.20 | ✓      | 59468.8    | 16.32        | 9.75          |
| restana                  | 4.9.9   | ✓      | 58656.0    | 16.57        | 10.46         |
| polka                    | 0.5.2   | ✓      | 57136.8    | 17.01        | 10.19         |
| micro                    | 9.4.1   | ✗      | 55646.4    | 17.47        | 9.92          |
| connect                  | 3.7.0   | ✗      | 55590.4    | 17.50        | 9.91          |
| server-base-router       | 7.1.32  | ✓      | 53337.6    | 18.25        | 9.51          |
| server-base              | 7.1.32  | ✗      | 53080.8    | 18.34        | 9.47          |
| fastify                  | 4.29.0  | ✓      | 52897.6    | 18.41        | 9.48          |
| yeps                     | 1.1.1   | ✗      | 51771.2    | 18.82        | 9.23          |
| connect-router           | 1.3.8   | ✓      | 50789.6    | 19.20        | 9.06          |
| micro-route              | 2.5.0   | ✓      | 48697.6    | 20.03        | 8.68          |
| trek-engine              | 1.0.5   | ✗      | 47375.8    | 20.61        | 7.77          |
| trek-router              | 1.2.0   | ✓      | 47288.6    | 20.65        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 45854.4    | 21.31        | 7.52          |
| yeps-router              | 1.2.0   | ✓      | 42895.0    | 22.82        | 7.65          |
| koa                      | 2.16.0  | ✗      | 40780.0    | 24.03        | 7.27          |
| spirit-router            | 0.5.0   | ✓      | 39868.0    | 24.59        | 7.11          |
| spirit                   | 0.6.1   | ✗      | 39666.4    | 24.71        | 7.07          |
| total.js                 | 3.4.13  | ✓      | 39049.6    | 25.11        | 11.95         |
| take-five                | 2.0.0   | ✓      | 38991.8    | 25.16        | 14.02         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38592.2    | 25.41        | 6.88          |
| restify                  | 8.6.1   | ✓      | 38563.8    | 25.43        | 6.95          |
| koa-router               | 12.0.1  | ✓      | 35338.2    | 27.80        | 6.30          |
| hapi                     | 20.3.0  | ✓      | 32070.4    | 30.68        | 5.72          |
| microrouter              | 3.1.3   | ✓      | 31783.6    | 30.96        | 5.67          |
| trpc-router              | 9.27.4  | ✓      | 26993.2    | 36.53        | 5.97          |
| egg.js                   | 3.30.1  | ✓      | 17061.7    | 58.09        | 6.10          |
| express                  | 4.21.2  | ✓      | 13646.2    | 72.72        | 2.43          |
| fastify-big-json         | 4.29.0  | ✓      | 12439.6    | 79.89        | 143.12        |
| express-with-middlewares | 4.21.2  | ✓      | 12379.4    | 80.20        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 10887.4    | 91.27        | 4.03          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

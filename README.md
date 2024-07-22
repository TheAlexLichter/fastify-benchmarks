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
* __Run:__ Mon Jul 22 2024 02:30:49 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69361.2    | 13.92        | 12.37         |
| polkadot                 | 1.0.0   | ✗      | 67684.4    | 14.28        | 12.07         |
| h3                       | 0.8.6   | ✗      | 66328.8    | 14.57        | 10.88         |
| h3-router                | 0.8.6   | ✓      | 65917.2    | 14.67        | 10.81         |
| restana                  | 4.9.9   | ✓      | 61752.0    | 15.69        | 11.01         |
| polka                    | 0.5.2   | ✓      | 59842.4    | 16.21        | 10.67         |
| bare                     | 10.13.0 | ✗      | 59463.2    | 16.32        | 10.60         |
| foxify                   | 0.10.20 | ✓      | 58895.2    | 16.48        | 9.66          |
| connect                  | 3.7.0   | ✗      | 57516.8    | 16.89        | 10.26         |
| micro                    | 9.4.1   | ✗      | 56356.0    | 17.25        | 10.05         |
| fastify                  | 4.28.1  | ✓      | 54947.2    | 17.70        | 9.85          |
| server-base-router       | 7.1.32  | ✓      | 54541.6    | 17.84        | 9.73          |
| server-base              | 7.1.32  | ✗      | 53279.2    | 18.27        | 9.50          |
| yeps                     | 1.1.1   | ✗      | 52961.6    | 18.38        | 9.44          |
| micro-route              | 2.5.0   | ✓      | 50489.6    | 19.30        | 9.00          |
| connect-router           | 1.3.8   | ✓      | 50484.0    | 19.30        | 9.00          |
| trek-engine              | 1.0.5   | ✗      | 48808.8    | 19.99        | 8.01          |
| trek-router              | 1.2.0   | ✓      | 47636.0    | 20.50        | 7.81          |
| vapr                     | 0.6.0   | ✓      | 45052.0    | 21.69        | 7.39          |
| spirit                   | 0.6.1   | ✗      | 44221.6    | 22.10        | 7.89          |
| yeps-router              | 1.2.0   | ✓      | 44034.4    | 22.21        | 7.85          |
| koa                      | 2.15.3  | ✗      | 43334.4    | 22.59        | 7.73          |
| spirit-router            | 0.5.0   | ✓      | 43008.0    | 22.74        | 7.67          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39800.2    | 24.62        | 7.10          |
| total.js                 | 3.4.13  | ✓      | 39299.2    | 24.95        | 12.03         |
| restify                  | 8.6.1   | ✓      | 39273.8    | 24.97        | 7.08          |
| take-five                | 2.0.0   | ✓      | 38965.0    | 25.17        | 14.01         |
| koa-router               | 12.0.1  | ✓      | 36895.0    | 26.60        | 6.58          |
| hapi                     | 20.3.0  | ✓      | 33765.6    | 29.11        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 32145.6    | 30.60        | 5.73          |
| trpc-router              | 9.27.4  | ✓      | 26268.0    | 37.55        | 5.81          |
| egg.js                   | 3.27.1  | ✓      | 17896.2    | 55.37        | 6.40          |
| express                  | 4.19.2  | ✓      | 13514.6    | 73.44        | 2.41          |
| fastify-big-json         | 4.28.1  | ✓      | 12971.0    | 76.54        | 149.24        |
| express-with-middlewares | 4.19.2  | ✓      | 12568.4    | 79.00        | 4.67          |
| express-route-prefix     | 4.19.2  | ✓      | 10959.2    | 90.67        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

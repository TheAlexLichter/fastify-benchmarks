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
* __Run:__ Mon Jan 12 2026 03:18:14 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66627.6    | 14.51        | 11.88         |
| polkadot                 | 1.0.0   | ✗      | 65310.8    | 14.81        | 11.65         |
| h3                       | 0.8.6   | ✗      | 64016.8    | 15.13        | 10.50         |
| h3-router                | 0.8.6   | ✓      | 63045.2    | 15.36        | 10.34         |
| foxify                   | 0.10.20 | ✓      | 59146.4    | 16.42        | 9.70          |
| bare                     | 10.13.0 | ✗      | 58361.6    | 16.64        | 10.41         |
| restana                  | 4.9.9   | ✓      | 58023.2    | 16.74        | 10.35         |
| micro                    | 9.4.1   | ✗      | 56248.0    | 17.28        | 10.03         |
| polka                    | 0.5.2   | ✓      | 56108.8    | 17.32        | 10.01         |
| connect                  | 3.7.0   | ✗      | 54944.8    | 17.71        | 9.80          |
| fastify                  | 4.29.1  | ✓      | 53444.8    | 18.21        | 9.58          |
| server-base-router       | 7.1.32  | ✓      | 52492.8    | 18.55        | 9.36          |
| server-base              | 7.1.32  | ✗      | 51480.0    | 18.93        | 9.18          |
| connect-router           | 1.3.8   | ✓      | 51282.4    | 19.00        | 9.14          |
| micro-route              | 2.5.0   | ✓      | 50475.2    | 19.31        | 9.00          |
| yeps                     | 1.1.1   | ✗      | 49479.2    | 19.71        | 8.82          |
| trek-engine              | 1.0.5   | ✗      | 45986.4    | 21.24        | 7.54          |
| trek-router              | 1.2.0   | ✓      | 44908.2    | 21.77        | 7.37          |
| vapr                     | 0.6.0   | ✓      | 44854.4    | 21.79        | 7.36          |
| koa                      | 2.16.3  | ✗      | 42099.0    | 23.26        | 7.51          |
| yeps-router              | 1.2.0   | ✓      | 41565.6    | 23.56        | 7.41          |
| spirit                   | 0.6.1   | ✗      | 39712.8    | 24.69        | 7.08          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38812.0    | 25.27        | 6.92          |
| total.js                 | 3.4.13  | ✓      | 38402.4    | 25.54        | 11.76         |
| spirit-router            | 0.5.0   | ✓      | 38396.0    | 25.54        | 6.85          |
| restify                  | 8.6.1   | ✓      | 37254.2    | 26.35        | 6.71          |
| take-five                | 2.0.0   | ✓      | 36923.8    | 26.58        | 13.27         |
| koa-router               | 12.0.1  | ✓      | 36312.6    | 27.04        | 6.48          |
| hapi                     | 20.3.0  | ✓      | 32817.4    | 29.97        | 5.85          |
| microrouter              | 3.1.3   | ✓      | 31890.6    | 30.85        | 5.69          |
| trpc-router              | 9.27.4  | ✓      | 25990.4    | 37.97        | 5.75          |
| egg.js                   | 3.32.0  | ✓      | 17309.4    | 57.24        | 6.19          |
| express                  | 4.22.1  | ✓      | 13358.4    | 74.29        | 2.38          |
| fastify-big-json         | 4.29.1  | ✓      | 12533.0    | 79.26        | 144.19        |
| express-with-middlewares | 4.22.1  | ✓      | 12346.8    | 80.45        | 4.59          |
| express-route-prefix     | 4.22.1  | ✓      | 10951.9    | 90.72        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Aug 18 2025 03:14:10 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 70121.2    | 13.76        | 12.50         |
| h3                       | 0.8.6   | ✗      | 67862.4    | 14.24        | 11.13         |
| h3-router                | 0.8.6   | ✓      | 66044.0    | 14.63        | 10.83         |
| restana                  | 4.9.9   | ✓      | 61269.6    | 15.82        | 10.93         |
| 0http                    | 3.5.3   | ✓      | 60503.2    | 16.03        | 10.79         |
| foxify                   | 0.10.20 | ✓      | 60021.6    | 16.16        | 9.85          |
| polka                    | 0.5.2   | ✓      | 58228.8    | 16.67        | 10.38         |
| fastify                  | 4.29.1  | ✓      | 58207.2    | 16.68        | 10.44         |
| micro                    | 9.4.1   | ✗      | 57235.2    | 16.97        | 10.21         |
| server-base              | 7.1.32  | ✗      | 56015.2    | 17.37        | 9.99          |
| yeps                     | 1.1.1   | ✗      | 55715.2    | 17.45        | 9.94          |
| bare                     | 10.13.0 | ✗      | 55592.0    | 17.49        | 9.91          |
| server-base-router       | 7.1.32  | ✓      | 54838.4    | 17.74        | 9.78          |
| connect                  | 3.7.0   | ✗      | 53826.4    | 18.08        | 9.60          |
| micro-route              | 2.5.0   | ✓      | 50033.6    | 19.49        | 8.92          |
| trek-engine              | 1.0.5   | ✗      | 49614.4    | 19.66        | 8.14          |
| trek-router              | 1.2.0   | ✓      | 48559.2    | 20.10        | 7.97          |
| connect-router           | 1.3.8   | ✓      | 48057.6    | 20.31        | 8.57          |
| vapr                     | 0.6.0   | ✓      | 47372.0    | 20.60        | 7.77          |
| spirit                   | 0.6.1   | ✗      | 45537.6    | 21.47        | 8.12          |
| yeps-router              | 1.2.0   | ✓      | 43880.8    | 22.29        | 7.83          |
| koa                      | 2.16.2  | ✗      | 43690.4    | 22.37        | 7.79          |
| spirit-router            | 0.5.0   | ✓      | 43392.0    | 22.57        | 7.74          |
| total.js                 | 3.4.13  | ✓      | 40136.8    | 24.42        | 12.29         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39876.6    | 24.58        | 7.11          |
| take-five                | 2.0.0   | ✓      | 39611.8    | 24.75        | 14.24         |
| restify                  | 8.6.1   | ✓      | 39324.0    | 24.92        | 7.09          |
| koa-router               | 12.0.1  | ✓      | 36073.4    | 27.22        | 6.43          |
| hapi                     | 20.3.0  | ✓      | 33926.2    | 28.98        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 31991.0    | 30.76        | 5.71          |
| trpc-router              | 9.27.4  | ✓      | 27977.6    | 35.24        | 6.19          |
| egg.js                   | 3.31.0  | ✓      | 16711.6    | 59.32        | 5.98          |
| express                  | 4.21.2  | ✓      | 13072.0    | 75.94        | 2.33          |
| fastify-big-json         | 4.29.1  | ✓      | 12788.4    | 77.65        | 147.14        |
| express-with-middlewares | 4.21.2  | ✓      | 12461.6    | 79.67        | 4.63          |
| express-route-prefix     | 4.21.2  | ✓      | 10959.5    | 90.66        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jan 19 2026 03:18:23 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68085.2    | 14.19        | 12.14         |
| h3                       | 0.8.6   | ✗      | 65413.2    | 14.78        | 10.73         |
| polkadot                 | 1.0.0   | ✗      | 61451.2    | 15.78        | 10.96         |
| bare                     | 10.13.0 | ✗      | 59643.2    | 16.27        | 10.64         |
| h3-router                | 0.8.6   | ✓      | 58610.4    | 16.57        | 9.61          |
| restana                  | 4.9.9   | ✓      | 58148.0    | 16.69        | 10.37         |
| foxify                   | 0.10.20 | ✓      | 57113.6    | 17.01        | 9.37          |
| polka                    | 0.5.2   | ✓      | 56501.6    | 17.20        | 10.08         |
| fastify                  | 4.29.1  | ✓      | 55523.2    | 17.51        | 9.95          |
| connect                  | 3.7.0   | ✗      | 55079.2    | 17.66        | 9.82          |
| server-base-router       | 7.1.32  | ✓      | 53924.0    | 18.05        | 9.62          |
| server-base              | 7.1.32  | ✗      | 53904.8    | 18.05        | 9.61          |
| micro                    | 9.4.1   | ✗      | 51088.0    | 19.07        | 9.11          |
| connect-router           | 1.3.8   | ✓      | 50276.8    | 19.39        | 8.97          |
| yeps                     | 1.1.1   | ✗      | 50198.4    | 19.42        | 8.95          |
| micro-route              | 2.5.0   | ✓      | 48720.8    | 20.03        | 8.69          |
| trek-engine              | 1.0.5   | ✗      | 47220.8    | 20.67        | 7.75          |
| trek-router              | 1.2.0   | ✓      | 46562.4    | 20.97        | 7.64          |
| vapr                     | 0.6.0   | ✓      | 46230.4    | 21.13        | 7.58          |
| yeps-router              | 1.2.0   | ✓      | 42364.0    | 23.10        | 7.55          |
| koa                      | 2.16.3  | ✗      | 39411.8    | 24.87        | 7.03          |
| spirit                   | 0.6.1   | ✗      | 39308.8    | 24.94        | 7.01          |
| total.js                 | 3.4.13  | ✓      | 38371.4    | 25.56        | 11.75         |
| take-five                | 2.0.0   | ✓      | 38335.8    | 25.59        | 13.78         |
| spirit-router            | 0.5.0   | ✓      | 37774.4    | 25.96        | 6.74          |
| restify                  | 8.6.1   | ✓      | 37382.2    | 26.25        | 6.74          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36275.4    | 27.07        | 6.47          |
| koa-router               | 12.0.1  | ✓      | 33782.2    | 29.11        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 31588.6    | 31.15        | 5.63          |
| hapi                     | 20.3.0  | ✓      | 30499.2    | 32.28        | 5.44          |
| trpc-router              | 9.27.4  | ✓      | 26640.4    | 37.03        | 5.89          |
| egg.js                   | 3.32.0  | ✓      | 17434.1    | 56.84        | 6.24          |
| express                  | 4.22.1  | ✓      | 13631.6    | 72.82        | 2.43          |
| fastify-big-json         | 4.29.1  | ✓      | 12435.2    | 79.88        | 143.09        |
| express-with-middlewares | 4.22.1  | ✓      | 12067.6    | 82.33        | 4.49          |
| express-route-prefix     | 4.22.1  | ✓      | 10788.1    | 92.12        | 3.99          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

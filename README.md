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
* __Run:__ Mon Mar 10 2025 02:25:32 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67584.8    | 14.30        | 12.05         |
| polkadot                 | 1.0.0   | ✗      | 65880.4    | 14.68        | 11.75         |
| h3                       | 0.8.6   | ✗      | 62786.4    | 15.44        | 10.30         |
| h3-router                | 0.8.6   | ✓      | 62703.2    | 15.44        | 10.28         |
| bare                     | 10.13.0 | ✗      | 61321.6    | 15.83        | 10.93         |
| restana                  | 4.9.9   | ✓      | 59668.8    | 16.26        | 10.64         |
| polka                    | 0.5.2   | ✓      | 59496.0    | 16.31        | 10.61         |
| connect                  | 3.7.0   | ✗      | 57873.6    | 16.77        | 10.32         |
| foxify                   | 0.10.20 | ✓      | 56975.2    | 17.05        | 9.35          |
| fastify                  | 4.29.0  | ✓      | 56468.0    | 17.22        | 10.12         |
| micro                    | 9.4.1   | ✗      | 55935.2    | 17.38        | 9.98          |
| server-base-router       | 7.1.32  | ✓      | 53484.8    | 18.20        | 9.54          |
| server-base              | 7.1.32  | ✗      | 53400.0    | 18.23        | 9.52          |
| yeps                     | 1.1.1   | ✗      | 52744.0    | 18.46        | 9.41          |
| connect-router           | 1.3.8   | ✓      | 52564.8    | 18.52        | 9.37          |
| micro-route              | 2.5.0   | ✓      | 51232.8    | 19.02        | 9.14          |
| trek-engine              | 1.0.5   | ✗      | 49064.0    | 19.88        | 8.05          |
| trek-router              | 1.2.0   | ✓      | 48175.2    | 20.26        | 7.90          |
| vapr                     | 0.6.0   | ✓      | 45972.8    | 21.26        | 7.54          |
| yeps-router              | 1.2.0   | ✓      | 44569.6    | 21.94        | 7.95          |
| spirit                   | 0.6.1   | ✗      | 43777.6    | 22.33        | 7.81          |
| spirit-router            | 0.5.0   | ✓      | 43435.2    | 22.52        | 7.75          |
| koa                      | 2.16.0  | ✗      | 42289.8    | 23.14        | 7.54          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40067.2    | 24.46        | 7.15          |
| total.js                 | 3.4.13  | ✓      | 39796.0    | 24.63        | 12.18         |
| take-five                | 2.0.0   | ✓      | 39128.6    | 25.06        | 14.07         |
| restify                  | 8.6.1   | ✓      | 38649.6    | 25.37        | 6.97          |
| koa-router               | 12.0.1  | ✓      | 37621.8    | 26.08        | 6.71          |
| hapi                     | 20.3.0  | ✓      | 34702.2    | 28.31        | 6.19          |
| microrouter              | 3.1.3   | ✓      | 32373.0    | 30.38        | 5.77          |
| trpc-router              | 9.27.4  | ✓      | 27368.4    | 36.03        | 6.05          |
| egg.js                   | 3.30.1  | ✓      | 17482.9    | 56.68        | 6.25          |
| express                  | 4.21.2  | ✓      | 13397.0    | 74.07        | 2.39          |
| fastify-big-json         | 4.29.0  | ✓      | 12464.6    | 79.66        | 143.41        |
| express-with-middlewares | 4.21.2  | ✓      | 12306.2    | 80.70        | 4.58          |
| express-route-prefix     | 4.21.2  | ✓      | 10987.6    | 90.42        | 4.07          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Aug 28 2023 02:06:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 49142.4    | 19.86        | 8.76          |
| micro                    | 9.4.1   | ✗      | 47531.2    | 20.55        | 8.48          |
| fastify                  | 4.22.0  | ✓      | 47296.0    | 20.66        | 8.48          |
| foxify                   | 0.10.20 | ✓      | 47188.8    | 20.69        | 7.74          |
| 0http                    | 3.5.2   | ✓      | 47148.8    | 20.72        | 8.41          |
| polka                    | 0.5.2   | ✓      | 47065.6    | 20.75        | 8.39          |
| polkadot                 | 1.0.0   | ✗      | 46304.0    | 21.11        | 8.26          |
| h3                       | 0.8.6   | ✗      | 46136.0    | 21.18        | 7.57          |
| server-base              | 7.1.32  | ✗      | 46004.8    | 21.24        | 8.20          |
| connect                  | 3.7.0   | ✗      | 45905.6    | 21.29        | 8.19          |
| h3-router                | 0.8.6   | ✓      | 44635.2    | 21.92        | 7.32          |
| server-base-router       | 7.1.32  | ✓      | 44338.4    | 22.05        | 7.91          |
| yeps                     | 1.1.1   | ✗      | 44072.0    | 22.19        | 7.86          |
| connect-router           | 1.3.8   | ✓      | 42566.4    | 23.00        | 7.59          |
| restana                  | 4.9.7   | ✓      | 42246.4    | 23.18        | 7.53          |
| micro-route              | 2.5.0   | ✓      | 40935.0    | 23.93        | 7.30          |
| trek-engine              | 1.0.5   | ✗      | 40012.2    | 24.50        | 6.56          |
| trek-router              | 1.2.0   | ✓      | 39531.8    | 24.82        | 6.48          |
| vapr                     | 0.6.0   | ✓      | 37622.2    | 26.08        | 6.17          |
| yeps-router              | 1.2.0   | ✓      | 36575.4    | 26.84        | 6.52          |
| koa                      | 2.14.2  | ✗      | 36096.6    | 27.20        | 6.44          |
| spirit                   | 0.6.1   | ✗      | 34136.2    | 28.82        | 6.09          |
| spirit-router            | 0.5.0   | ✓      | 33307.8    | 29.58        | 5.94          |
| take-five                | 2.0.0   | ✓      | 32453.4    | 30.32        | 11.67         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 31951.2    | 30.79        | 5.70          |
| total.js                 | 3.4.13  | ✓      | 31622.4    | 31.12        | 9.68          |
| restify                  | 8.6.1   | ✓      | 31217.2    | 31.56        | 5.63          |
| koa-router               | 12.0.0  | ✓      | 29047.2    | 33.95        | 5.18          |
| hapi                     | 20.3.0  | ✓      | 25878.9    | 38.13        | 4.62          |
| microrouter              | 3.1.3   | ✓      | 24824.4    | 39.78        | 4.43          |
| trpc-router              | 9.27.3  | ✓      | 21416.0    | 46.19        | 4.74          |
| egg.js                   | 3.17.4  | ✓      | 12845.0    | 77.37        | 4.59          |
| express                  | 4.18.2  | ✓      | 10295.1    | 96.55        | 1.84          |
| express-with-middlewares | 4.18.2  | ✓      | 8938.5     | 111.30       | 3.32          |
| express-route-prefix     | 4.18.2  | ✓      | 8511.4     | 116.92       | 3.15          |
| fastify-big-json         | 4.22.0  | ✓      | 8452.3     | 117.87       | 97.25         |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

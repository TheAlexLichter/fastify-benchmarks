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
* __Node:__ `v14.21.2`
* __Run:__ Mon Jan 23 2023 02:33:10 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 56064.0    | 17.35        | 10.00         |
| connect                  | 3.7.0   | ✗      | 55845.6    | 17.42        | 9.96          |
| foxify                   | 0.10.20 | ✓      | 55118.4    | 17.65        | 9.04          |
| polkadot                 | 1.0.0   | ✗      | 54810.4    | 17.75        | 9.78          |
| polka                    | 0.5.2   | ✓      | 54421.6    | 17.88        | 9.71          |
| 0http                    | 3.4.2   | ✓      | 54114.4    | 17.99        | 9.65          |
| micro                    | 9.4.1   | ✗      | 53795.2    | 18.10        | 9.59          |
| h3                       | 0.8.6   | ✗      | 52507.2    | 18.55        | 8.61          |
| server-base              | 7.1.32  | ✗      | 51433.6    | 18.94        | 9.17          |
| h3-router                | 0.8.6   | ✓      | 50794.4    | 19.19        | 8.33          |
| server-base-router       | 7.1.32  | ✓      | 49944.0    | 19.52        | 8.91          |
| yeps                     | 1.1.1   | ✗      | 49532.8    | 19.69        | 8.83          |
| restana                  | 4.9.7   | ✓      | 49443.2    | 19.73        | 8.82          |
| connect-router           | 1.3.7   | ✓      | 48783.2    | 20.00        | 8.70          |
| micro-route              | 2.5.0   | ✓      | 47582.4    | 20.52        | 8.49          |
| trek-engine              | 1.0.5   | ✗      | 44198.6    | 22.13        | 7.25          |
| trek-router              | 1.2.0   | ✓      | 43762.6    | 22.35        | 7.18          |
| vapr                     | 0.6.0   | ✓      | 42529.6    | 23.01        | 6.98          |
| yeps-router              | 1.2.0   | ✓      | 41297.6    | 23.72        | 7.37          |
| fastify                  | 4.12.0  | ✓      | 39651.2    | 24.72        | 7.11          |
| koa                      | 2.14.1  | ✗      | 38766.6    | 25.31        | 6.91          |
| take-five                | 2.0.0   | ✓      | 36710.2    | 26.74        | 13.20         |
| total.js                 | 3.4.13  | ✓      | 36619.0    | 26.81        | 11.21         |
| spirit                   | 0.6.1   | ✗      | 36431.2    | 26.96        | 6.50          |
| spirit-router            | 0.5.0   | ✓      | 36389.0    | 26.99        | 6.49          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 35895.0    | 27.35        | 6.40          |
| restify                  | 8.6.1   | ✓      | 34786.2    | 28.24        | 6.27          |
| koa-router               | 12.0.0  | ✓      | 33130.2    | 29.69        | 5.91          |
| hapi                     | 20.2.2  | ✓      | 29439.2    | 33.48        | 5.25          |
| microrouter              | 3.1.3   | ✓      | 27842.4    | 35.41        | 4.97          |
| trpc-router              | 9.27.3  | ✓      | 21675.6    | 45.62        | 4.80          |
| egg.js                   | 3.14.2  | ✓      | 14272.4    | 69.58        | 5.10          |
| express                  | 4.18.2  | ✓      | 11917.8    | 83.35        | 2.13          |
| express-with-middlewares | 4.18.2  | ✓      | 10397.1    | 95.58        | 3.87          |
| express-route-prefix     | 4.18.2  | ✓      | 10107.8    | 98.39        | 3.74          |
| fastify-big-json         | 4.12.0  | ✓      | 9852.4     | 100.99       | 113.36        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

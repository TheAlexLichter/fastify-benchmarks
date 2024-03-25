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
* __Run:__ Mon Mar 25 2024 02:08:33 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68519.2    | 14.10        | 12.22         |
| h3-router                | 0.8.6   | ✓      | 64326.8    | 15.06        | 10.55         |
| 0http                    | 3.5.2   | ✓      | 62444.8    | 15.52        | 11.14         |
| h3                       | 0.8.6   | ✗      | 62217.6    | 15.58        | 10.21         |
| bare                     | 10.13.0 | ✗      | 60257.6    | 16.09        | 10.75         |
| foxify                   | 0.10.20 | ✓      | 58627.2    | 16.57        | 9.62          |
| polka                    | 0.5.2   | ✓      | 56866.4    | 17.09        | 10.14         |
| fastify                  | 4.26.2  | ✓      | 56415.2    | 17.23        | 10.11         |
| connect                  | 3.7.0   | ✗      | 55980.8    | 17.36        | 9.98          |
| micro                    | 9.4.1   | ✗      | 55094.4    | 17.65        | 9.82          |
| restana                  | 4.9.7   | ✓      | 55000.8    | 17.69        | 9.81          |
| server-base              | 7.1.32  | ✗      | 51507.2    | 18.92        | 9.19          |
| server-base-router       | 7.1.32  | ✓      | 51226.4    | 19.02        | 9.13          |
| connect-router           | 1.3.8   | ✓      | 50174.4    | 19.43        | 8.95          |
| yeps                     | 1.1.1   | ✗      | 50072.8    | 19.47        | 8.93          |
| micro-route              | 2.5.0   | ✓      | 49416.8    | 19.74        | 8.81          |
| trek-engine              | 1.0.5   | ✗      | 46716.6    | 20.91        | 7.66          |
| trek-router              | 1.2.0   | ✓      | 44696.8    | 21.88        | 7.33          |
| vapr                     | 0.6.0   | ✓      | 44005.6    | 22.22        | 7.22          |
| yeps-router              | 1.2.0   | ✓      | 43698.4    | 22.39        | 7.79          |
| koa                      | 2.15.2  | ✗      | 41663.2    | 23.50        | 7.43          |
| spirit                   | 0.6.1   | ✗      | 41143.2    | 23.80        | 7.34          |
| spirit-router            | 0.5.0   | ✓      | 39629.6    | 24.74        | 7.07          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38562.6    | 25.43        | 6.88          |
| restify                  | 8.6.1   | ✓      | 38112.2    | 25.74        | 6.87          |
| total.js                 | 3.4.13  | ✓      | 37884.6    | 25.89        | 11.60         |
| koa-router               | 12.0.1  | ✓      | 37412.2    | 26.23        | 6.67          |
| take-five                | 2.0.0   | ✓      | 37292.2    | 26.32        | 13.41         |
| hapi                     | 20.3.0  | ✓      | 32435.2    | 30.33        | 5.78          |
| microrouter              | 3.1.3   | ✓      | 32139.8    | 30.61        | 5.73          |
| trpc-router              | 9.27.4  | ✓      | 25961.2    | 38.01        | 5.74          |
| egg.js                   | 3.20.0  | ✓      | 17612.5    | 56.27        | 6.30          |
| express                  | 4.19.1  | ✓      | 13233.4    | 75.01        | 2.36          |
| fastify-big-json         | 4.26.2  | ✓      | 12978.4    | 76.52        | 149.32        |
| express-with-middlewares | 4.19.1  | ✓      | 12381.2    | 80.21        | 4.60          |
| express-route-prefix     | 4.19.1  | ✓      | 11044.0    | 89.98        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

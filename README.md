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
* __Run:__ Mon Sep 11 2023 02:07:11 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 63227.2    | 15.30        | 11.28         |
| bare                     | 10.13.0 | ✗      | 60453.6    | 16.05        | 10.78         |
| 0http                    | 3.5.2   | ✓      | 60292.0    | 16.12        | 10.75         |
| h3                       | 0.8.6   | ✗      | 59273.6    | 16.38        | 9.72          |
| foxify                   | 0.10.20 | ✓      | 58905.6    | 16.48        | 9.66          |
| polka                    | 0.5.2   | ✓      | 58780.0    | 16.51        | 10.48         |
| h3-router                | 0.8.6   | ✓      | 58547.2    | 16.59        | 9.60          |
| connect                  | 3.7.0   | ✗      | 58171.2    | 16.69        | 10.37         |
| fastify                  | 4.22.2  | ✓      | 57639.2    | 16.85        | 10.33         |
| micro                    | 9.4.1   | ✗      | 56288.0    | 17.27        | 10.04         |
| server-base              | 7.1.32  | ✗      | 55997.6    | 17.36        | 9.99          |
| server-base-router       | 7.1.32  | ✓      | 55467.2    | 17.53        | 9.89          |
| yeps                     | 1.1.1   | ✗      | 54095.2    | 17.99        | 9.65          |
| restana                  | 4.9.7   | ✓      | 53966.4    | 18.07        | 9.62          |
| connect-router           | 1.3.8   | ✓      | 51451.2    | 18.94        | 9.18          |
| micro-route              | 2.5.0   | ✓      | 51152.0    | 19.06        | 9.12          |
| trek-engine              | 1.0.5   | ✗      | 48462.6    | 20.14        | 7.95          |
| vapr                     | 0.6.0   | ✓      | 48174.4    | 20.26        | 7.90          |
| trek-router              | 1.2.0   | ✓      | 47319.4    | 20.64        | 7.76          |
| yeps-router              | 1.2.0   | ✓      | 44203.2    | 22.13        | 7.88          |
| koa                      | 2.14.2  | ✗      | 43731.2    | 22.37        | 7.80          |
| spirit                   | 0.6.1   | ✗      | 43667.2    | 22.41        | 7.79          |
| spirit-router            | 0.5.0   | ✓      | 41520.8    | 23.59        | 7.40          |
| take-five                | 2.0.0   | ✓      | 41118.4    | 23.82        | 14.78         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40545.4    | 24.17        | 7.23          |
| total.js                 | 3.4.13  | ✓      | 40539.2    | 24.18        | 12.41         |
| restify                  | 8.6.1   | ✓      | 39625.6    | 24.73        | 7.14          |
| koa-router               | 12.0.0  | ✓      | 36691.8    | 26.76        | 6.54          |
| hapi                     | 20.3.0  | ✓      | 33901.0    | 28.99        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 31993.2    | 30.76        | 5.71          |
| trpc-router              | 9.27.3  | ✓      | 27263.6    | 36.17        | 6.03          |
| egg.js                   | 3.17.4  | ✓      | 16359.8    | 60.60        | 5.85          |
| express                  | 4.18.2  | ✓      | 13781.2    | 72.00        | 2.46          |
| express-with-middlewares | 4.18.2  | ✓      | 12065.4    | 82.34        | 4.49          |
| fastify-big-json         | 4.22.2  | ✓      | 11840.2    | 83.99        | 136.23        |
| express-route-prefix     | 4.18.2  | ✓      | 11789.4    | 84.27        | 4.36          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

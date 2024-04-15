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
* __Run:__ Mon Apr 15 2024 04:24:14 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67278.0    | 14.38        | 12.00         |
| 0http                    | 3.5.3   | ✓      | 67083.6    | 14.42        | 11.96         |
| h3-router                | 0.8.6   | ✓      | 64130.8    | 15.11        | 10.52         |
| h3                       | 0.8.6   | ✗      | 62142.4    | 15.60        | 10.19         |
| bare                     | 10.13.0 | ✗      | 60844.0    | 15.94        | 10.85         |
| restana                  | 4.9.9   | ✓      | 59778.4    | 16.25        | 10.66         |
| foxify                   | 0.10.20 | ✓      | 57458.4    | 16.90        | 9.42          |
| connect                  | 3.7.0   | ✗      | 56763.2    | 17.11        | 10.12         |
| polka                    | 0.5.2   | ✓      | 56571.2    | 17.18        | 10.09         |
| fastify                  | 4.26.2  | ✓      | 54903.2    | 17.73        | 9.84          |
| micro                    | 9.4.1   | ✗      | 54576.0    | 17.83        | 9.73          |
| server-base-router       | 7.1.32  | ✓      | 52927.2    | 18.40        | 9.44          |
| server-base              | 7.1.32  | ✗      | 52595.2    | 18.52        | 9.38          |
| yeps                     | 1.1.1   | ✗      | 52464.0    | 18.55        | 9.36          |
| connect-router           | 1.3.8   | ✓      | 50920.8    | 19.14        | 9.08          |
| micro-route              | 2.5.0   | ✓      | 50031.2    | 19.49        | 8.92          |
| trek-router              | 1.2.0   | ✓      | 47835.2    | 20.41        | 7.85          |
| trek-engine              | 1.0.5   | ✗      | 46408.0    | 21.05        | 7.61          |
| vapr                     | 0.6.0   | ✓      | 45568.0    | 21.45        | 7.47          |
| yeps-router              | 1.2.0   | ✓      | 44532.8    | 21.97        | 7.94          |
| spirit                   | 0.6.1   | ✗      | 44393.6    | 22.06        | 7.92          |
| koa                      | 2.15.3  | ✗      | 42466.4    | 23.06        | 7.57          |
| spirit-router            | 0.5.0   | ✓      | 41463.2    | 23.62        | 7.39          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40491.2    | 24.21        | 7.22          |
| restify                  | 8.6.1   | ✓      | 39342.2    | 24.93        | 7.09          |
| total.js                 | 3.4.13  | ✓      | 38832.0    | 25.25        | 11.89         |
| take-five                | 2.0.0   | ✓      | 37952.6    | 25.85        | 13.64         |
| koa-router               | 12.0.1  | ✓      | 37410.2    | 26.23        | 6.67          |
| hapi                     | 20.3.0  | ✓      | 33552.8    | 29.29        | 5.98          |
| microrouter              | 3.1.3   | ✓      | 31874.0    | 30.87        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 26719.2    | 36.91        | 5.91          |
| egg.js                   | 3.22.0  | ✓      | 17357.8    | 57.09        | 6.21          |
| express                  | 4.19.2  | ✓      | 13801.8    | 71.91        | 2.46          |
| fastify-big-json         | 4.26.2  | ✓      | 12801.4    | 77.56        | 147.29        |
| express-with-middlewares | 4.19.2  | ✓      | 12635.0    | 78.58        | 4.70          |
| express-route-prefix     | 4.19.2  | ✓      | 11026.0    | 90.11        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

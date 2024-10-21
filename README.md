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
* __Run:__ Mon Oct 21 2024 02:41:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67305.2    | 14.37        | 12.00         |
| 0http                    | 3.5.3   | ✓      | 67204.0    | 14.39        | 11.98         |
| h3                       | 0.8.6   | ✗      | 64475.6    | 15.01        | 10.58         |
| h3-router                | 0.8.6   | ✓      | 64080.4    | 15.13        | 10.51         |
| restana                  | 4.9.9   | ✓      | 60358.4    | 16.08        | 10.76         |
| bare                     | 10.13.0 | ✗      | 60304.8    | 16.07        | 10.75         |
| foxify                   | 0.10.20 | ✓      | 58903.2    | 16.48        | 9.66          |
| polka                    | 0.5.2   | ✓      | 58386.4    | 16.63        | 10.41         |
| connect                  | 3.7.0   | ✗      | 58317.6    | 16.65        | 10.40         |
| server-base              | 7.1.32  | ✗      | 55146.4    | 17.63        | 9.84          |
| micro                    | 9.4.1   | ✗      | 54990.4    | 17.69        | 9.81          |
| server-base-router       | 7.1.32  | ✓      | 54784.8    | 17.75        | 9.77          |
| fastify                  | 4.28.1  | ✓      | 53885.6    | 18.06        | 9.66          |
| yeps                     | 1.1.1   | ✗      | 53257.6    | 18.27        | 9.50          |
| connect-router           | 1.3.8   | ✓      | 50036.8    | 19.49        | 8.92          |
| micro-route              | 2.5.0   | ✓      | 49686.4    | 19.62        | 8.86          |
| trek-engine              | 1.0.5   | ✗      | 48818.4    | 19.99        | 8.01          |
| trek-router              | 1.2.0   | ✓      | 47917.6    | 20.37        | 7.86          |
| vapr                     | 0.6.0   | ✓      | 46345.6    | 21.07        | 7.60          |
| yeps-router              | 1.2.0   | ✓      | 44302.4    | 22.09        | 7.90          |
| spirit                   | 0.6.1   | ✗      | 42600.0    | 22.95        | 7.60          |
| koa                      | 2.15.3  | ✗      | 42460.8    | 23.05        | 7.57          |
| spirit-router            | 0.5.0   | ✓      | 41240.8    | 23.72        | 7.36          |
| restify                  | 8.6.1   | ✓      | 39326.4    | 24.93        | 7.09          |
| total.js                 | 3.4.13  | ✓      | 39173.6    | 25.03        | 11.99         |
| take-five                | 2.0.0   | ✓      | 38913.8    | 25.19        | 13.99         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38399.8    | 25.54        | 6.85          |
| koa-router               | 12.0.1  | ✓      | 37831.2    | 25.93        | 6.75          |
| hapi                     | 20.3.0  | ✓      | 32214.2    | 30.54        | 5.74          |
| microrouter              | 3.1.3   | ✓      | 30783.6    | 31.97        | 5.49          |
| trpc-router              | 9.27.4  | ✓      | 26784.8    | 36.83        | 5.93          |
| egg.js                   | 3.28.0  | ✓      | 17705.1    | 55.95        | 6.33          |
| express                  | 4.21.1  | ✓      | 13870.4    | 71.54        | 2.47          |
| fastify-big-json         | 4.28.1  | ✓      | 12806.0    | 77.55        | 147.34        |
| express-with-middlewares | 4.21.1  | ✓      | 12522.4    | 79.28        | 4.66          |
| express-route-prefix     | 4.21.1  | ✓      | 10794.0    | 92.07        | 3.99          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Aug 12 2024 02:30:06 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68758.8    | 14.05        | 12.26         |
| h3-router                | 0.8.6   | ✓      | 64211.6    | 15.08        | 10.53         |
| polkadot                 | 1.0.0   | ✗      | 63468.0    | 15.25        | 11.32         |
| h3                       | 0.8.6   | ✗      | 62746.4    | 15.43        | 10.29         |
| bare                     | 10.13.0 | ✗      | 60130.4    | 16.13        | 10.72         |
| restana                  | 4.9.9   | ✓      | 59868.0    | 16.22        | 10.68         |
| foxify                   | 0.10.20 | ✓      | 59351.2    | 16.35        | 9.73          |
| connect                  | 3.7.0   | ✗      | 58615.2    | 16.56        | 10.45         |
| polka                    | 0.5.2   | ✓      | 58512.8    | 16.59        | 10.43         |
| fastify                  | 4.28.1  | ✓      | 55959.2    | 17.37        | 10.03         |
| server-base-router       | 7.1.32  | ✓      | 55788.8    | 17.43        | 9.95          |
| micro                    | 9.4.1   | ✗      | 54543.2    | 17.84        | 9.73          |
| server-base              | 7.1.32  | ✗      | 54105.6    | 17.98        | 9.65          |
| yeps                     | 1.1.1   | ✗      | 50204.8    | 19.42        | 8.95          |
| connect-router           | 1.3.8   | ✓      | 49942.4    | 19.52        | 8.91          |
| micro-route              | 2.5.0   | ✓      | 49212.8    | 19.83        | 8.78          |
| trek-router              | 1.2.0   | ✓      | 47829.6    | 20.41        | 7.85          |
| trek-engine              | 1.0.5   | ✗      | 47119.2    | 20.73        | 7.73          |
| vapr                     | 0.6.0   | ✓      | 45169.6    | 21.63        | 7.41          |
| yeps-router              | 1.2.0   | ✓      | 43812.8    | 22.32        | 7.81          |
| spirit                   | 0.6.1   | ✗      | 43160.8    | 22.66        | 7.70          |
| spirit-router            | 0.5.0   | ✓      | 41954.4    | 23.33        | 7.48          |
| koa                      | 2.15.3  | ✗      | 41897.4    | 23.37        | 7.47          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39585.0    | 24.76        | 7.06          |
| total.js                 | 3.4.13  | ✓      | 39263.0    | 24.97        | 12.02         |
| take-five                | 2.0.0   | ✓      | 38035.8    | 25.79        | 13.68         |
| restify                  | 8.6.1   | ✓      | 37657.4    | 26.05        | 6.79          |
| koa-router               | 12.0.1  | ✓      | 37027.8    | 26.50        | 6.60          |
| hapi                     | 20.3.0  | ✓      | 33192.2    | 29.62        | 5.92          |
| microrouter              | 3.1.3   | ✓      | 31698.0    | 31.05        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 26317.2    | 37.49        | 5.82          |
| egg.js                   | 3.27.1  | ✓      | 17223.8    | 57.55        | 6.16          |
| express                  | 4.19.2  | ✓      | 13488.2    | 73.58        | 2.41          |
| fastify-big-json         | 4.28.1  | ✓      | 12952.2    | 76.67        | 149.03        |
| express-with-middlewares | 4.19.2  | ✓      | 12627.4    | 78.64        | 4.70          |
| express-route-prefix     | 4.19.2  | ✓      | 11057.2    | 89.86        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jun 29 2026 05:40:42 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 74874.8    | 12.85        | 13.35         |
| polkadot                 | 1.0.0   | ✗      | 73435.6    | 13.12        | 13.10         |
| h3                       | 0.8.6   | ✗      | 71094.0    | 13.55        | 11.66         |
| connect                  | 3.7.0   | ✗      | 70742.8    | 13.64        | 12.62         |
| polka                    | 0.5.2   | ✓      | 70686.0    | 13.65        | 12.60         |
| h3-router                | 0.8.6   | ✓      | 69860.4    | 13.81        | 11.46         |
| bare                     | 10.13.0 | ✗      | 69683.6    | 13.86        | 12.43         |
| restana                  | 4.9.9   | ✓      | 69177.2    | 13.98        | 12.34         |
| foxify                   | 0.10.20 | ✓      | 68348.4    | 14.14        | 11.21         |
| fastify                  | 4.29.1  | ✓      | 68062.0    | 14.19        | 12.20         |
| server-base              | 7.1.32  | ✗      | 67082.4    | 14.41        | 11.96         |
| server-base-router       | 7.1.32  | ✓      | 66499.2    | 14.54        | 11.86         |
| micro                    | 9.4.1   | ✗      | 65943.6    | 14.67        | 11.76         |
| connect-router           | 1.3.8   | ✓      | 63722.4    | 15.20        | 11.36         |
| yeps                     | 1.1.1   | ✗      | 63289.2    | 15.31        | 11.29         |
| micro-route              | 2.5.0   | ✓      | 61144.0    | 15.86        | 10.90         |
| vapr                     | 0.6.0   | ✓      | 58143.2    | 16.71        | 9.54          |
| trek-engine              | 1.0.5   | ✗      | 56697.6    | 17.14        | 9.30          |
| trek-router              | 1.2.0   | ✓      | 55106.4    | 17.65        | 9.04          |
| yeps-router              | 1.2.0   | ✓      | 51896.8    | 18.76        | 9.26          |
| koa                      | 2.16.4  | ✗      | 51270.4    | 19.00        | 9.14          |
| total.js                 | 3.4.13  | ✓      | 51265.6    | 19.01        | 15.69         |
| take-five                | 2.0.0   | ✓      | 51064.8    | 19.08        | 18.36         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 47038.4    | 20.76        | 8.39          |
| restify                  | 8.6.1   | ✓      | 45727.2    | 21.37        | 8.24          |
| spirit                   | 0.6.1   | ✗      | 43953.6    | 22.21        | 7.84          |
| koa-router               | 12.0.1  | ✓      | 43844.8    | 22.31        | 7.82          |
| spirit-router            | 0.5.0   | ✓      | 43361.6    | 22.57        | 7.73          |
| microrouter              | 3.1.3   | ✓      | 41676.0    | 23.50        | 7.43          |
| hapi                     | 20.3.0  | ✓      | 38958.6    | 25.17        | 6.95          |
| trpc-router              | 9.27.4  | ✓      | 32058.8    | 30.69        | 7.09          |
| egg.js                   | 3.34.0  | ✓      | 19319.6    | 51.23        | 6.91          |
| express                  | 4.22.2  | ✓      | 16920.1    | 58.57        | 3.02          |
| express-with-middlewares | 4.22.2  | ✓      | 15602.7    | 63.56        | 5.80          |
| fastify-big-json         | 4.29.1  | ✓      | 13155.0    | 75.47        | 151.36        |
| express-route-prefix     | 4.22.2  | ✓      | 12323.8    | 80.57        | 4.56          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

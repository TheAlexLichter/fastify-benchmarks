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
* __Run:__ Mon Oct 20 2025 02:56:56 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68176.4    | 14.17        | 12.16         |
| polkadot                 | 1.0.0   | ✗      | 66184.8    | 14.61        | 11.80         |
| h3                       | 0.8.6   | ✗      | 60611.2    | 16.00        | 9.94          |
| restana                  | 4.9.9   | ✓      | 60436.0    | 16.05        | 10.78         |
| bare                     | 10.13.0 | ✗      | 58846.4    | 16.50        | 10.49         |
| h3-router                | 0.8.6   | ✓      | 58676.0    | 16.54        | 9.63          |
| foxify                   | 0.10.20 | ✓      | 57210.4    | 16.98        | 9.38          |
| polka                    | 0.5.2   | ✓      | 56957.6    | 17.06        | 10.16         |
| connect                  | 3.7.0   | ✗      | 56555.2    | 17.19        | 10.09         |
| fastify                  | 4.29.1  | ✓      | 54084.8    | 17.99        | 9.70          |
| server-base              | 7.1.32  | ✗      | 53855.2    | 18.07        | 9.60          |
| server-base-router       | 7.1.32  | ✓      | 53730.4    | 18.11        | 9.58          |
| micro                    | 9.4.1   | ✗      | 52913.6    | 18.40        | 9.44          |
| yeps                     | 1.1.1   | ✗      | 52350.4    | 18.61        | 9.34          |
| connect-router           | 1.3.8   | ✓      | 48896.8    | 19.96        | 8.72          |
| micro-route              | 2.5.0   | ✓      | 48485.6    | 20.13        | 8.65          |
| vapr                     | 0.6.0   | ✓      | 47446.4    | 20.58        | 7.78          |
| trek-engine              | 1.0.5   | ✗      | 46167.2    | 21.16        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 45383.2    | 21.56        | 8.09          |
| trek-router              | 1.2.0   | ✓      | 45166.4    | 21.64        | 7.41          |
| yeps-router              | 1.2.0   | ✓      | 43924.0    | 22.26        | 7.83          |
| spirit-router            | 0.5.0   | ✓      | 43781.6    | 22.32        | 7.81          |
| koa                      | 2.16.3  | ✗      | 41389.8    | 23.66        | 7.38          |
| total.js                 | 3.4.13  | ✓      | 40308.0    | 24.31        | 12.34         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38469.0    | 25.50        | 6.86          |
| restify                  | 8.6.1   | ✓      | 38397.4    | 25.54        | 6.92          |
| take-five                | 2.0.0   | ✓      | 38113.0    | 25.74        | 13.70         |
| koa-router               | 12.0.1  | ✓      | 35710.6    | 27.50        | 6.37          |
| hapi                     | 20.3.0  | ✓      | 32195.4    | 30.56        | 5.74          |
| microrouter              | 3.1.3   | ✓      | 31677.8    | 31.06        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 27260.0    | 36.18        | 6.03          |
| egg.js                   | 3.31.0  | ✓      | 17241.5    | 57.47        | 6.17          |
| express                  | 4.21.2  | ✓      | 13098.0    | 75.81        | 2.34          |
| fastify-big-json         | 4.29.1  | ✓      | 12424.2    | 79.94        | 142.95        |
| express-with-middlewares | 4.21.2  | ✓      | 12266.4    | 80.96        | 4.56          |
| express-route-prefix     | 4.21.2  | ✓      | 10636.4    | 93.45        | 3.94          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

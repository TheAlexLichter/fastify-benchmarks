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
* __Run:__ Mon Jul 01 2024 02:32:09 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67880.0    | 14.23        | 12.10         |
| polkadot                 | 1.0.0   | ✗      | 67685.6    | 14.29        | 12.07         |
| h3                       | 0.8.6   | ✗      | 63133.2    | 15.34        | 10.36         |
| h3-router                | 0.8.6   | ✓      | 62607.2    | 15.47        | 10.27         |
| restana                  | 4.9.9   | ✓      | 61098.4    | 15.86        | 10.90         |
| bare                     | 10.13.0 | ✗      | 59872.8    | 16.20        | 10.68         |
| connect                  | 3.7.0   | ✗      | 57584.8    | 16.88        | 10.27         |
| polka                    | 0.5.2   | ✓      | 57172.8    | 17.00        | 10.20         |
| foxify                   | 0.10.20 | ✓      | 56276.0    | 17.27        | 9.23          |
| micro                    | 9.4.1   | ✗      | 56268.8    | 17.28        | 10.03         |
| server-base              | 7.1.32  | ✗      | 55393.6    | 17.57        | 9.88          |
| server-base-router       | 7.1.32  | ✓      | 54923.2    | 17.73        | 9.79          |
| fastify                  | 4.28.1  | ✓      | 54809.6    | 17.75        | 9.83          |
| yeps                     | 1.1.1   | ✗      | 51137.6    | 19.06        | 9.12          |
| connect-router           | 1.3.8   | ✓      | 50473.6    | 19.31        | 9.00          |
| micro-route              | 2.5.0   | ✓      | 50030.4    | 19.48        | 8.92          |
| trek-engine              | 1.0.5   | ✗      | 48359.2    | 20.18        | 7.93          |
| trek-router              | 1.2.0   | ✓      | 47034.4    | 20.77        | 7.71          |
| vapr                     | 0.6.0   | ✓      | 45084.0    | 21.67        | 7.40          |
| yeps-router              | 1.2.0   | ✓      | 43544.8    | 22.47        | 7.77          |
| koa                      | 2.15.3  | ✗      | 42682.4    | 22.93        | 7.61          |
| spirit                   | 0.6.1   | ✗      | 42050.4    | 23.29        | 7.50          |
| spirit-router            | 0.5.0   | ✓      | 40470.4    | 24.21        | 7.22          |
| total.js                 | 3.4.13  | ✓      | 40192.8    | 24.37        | 12.30         |
| restify                  | 8.6.1   | ✓      | 39666.6    | 24.71        | 7.15          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39441.6    | 24.85        | 7.03          |
| take-five                | 2.0.0   | ✓      | 38661.8    | 25.35        | 13.90         |
| koa-router               | 12.0.1  | ✓      | 37678.2    | 26.04        | 6.72          |
| hapi                     | 20.3.0  | ✓      | 33684.6    | 29.19        | 6.01          |
| microrouter              | 3.1.3   | ✓      | 31863.4    | 30.88        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 26922.4    | 36.63        | 5.96          |
| egg.js                   | 3.25.0  | ✓      | 17076.9    | 58.03        | 6.11          |
| express                  | 4.19.2  | ✓      | 13586.4    | 73.04        | 2.42          |
| fastify-big-json         | 4.28.1  | ✓      | 12539.6    | 79.21        | 144.28        |
| express-with-middlewares | 4.19.2  | ✓      | 12050.2    | 82.44        | 4.48          |
| express-route-prefix     | 4.19.2  | ✓      | 10722.5    | 92.67        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

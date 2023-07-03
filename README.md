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
* __Run:__ Mon Jul 03 2023 02:48:34 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 63468.0    | 15.24        | 11.32         |
| bare                     | 10.13.0 | ✗      | 60847.2    | 15.94        | 10.85         |
| 0http                    | 3.5.2   | ✓      | 60708.8    | 15.99        | 10.83         |
| h3                       | 0.8.6   | ✗      | 59794.4    | 16.23        | 9.81          |
| h3-router                | 0.8.6   | ✓      | 58967.2    | 16.47        | 9.67          |
| polka                    | 0.5.2   | ✓      | 58528.8    | 16.59        | 10.44         |
| foxify                   | 0.10.20 | ✓      | 58024.0    | 16.74        | 9.52          |
| fastify                  | 4.19.1  | ✓      | 57908.8    | 16.77        | 10.38         |
| micro                    | 9.4.1   | ✗      | 56746.4    | 17.13        | 10.12         |
| connect                  | 3.7.0   | ✗      | 56476.6    | 17.22        | 10.07         |
| restana                  | 4.9.7   | ✓      | 55414.4    | 17.50        | 9.88          |
| yeps                     | 1.1.1   | ✗      | 54935.2    | 17.70        | 9.80          |
| server-base              | 7.1.32  | ✗      | 54927.2    | 17.70        | 9.80          |
| server-base-router       | 7.1.32  | ✓      | 54190.4    | 17.96        | 9.66          |
| connect-router           | 1.3.8   | ✓      | 51805.6    | 18.81        | 9.24          |
| micro-route              | 2.5.0   | ✓      | 50592.8    | 19.27        | 9.02          |
| trek-engine              | 1.0.5   | ✗      | 49318.4    | 19.78        | 8.09          |
| trek-router              | 1.2.0   | ✓      | 48643.4    | 20.06        | 7.98          |
| vapr                     | 0.6.0   | ✓      | 47716.0    | 20.47        | 7.83          |
| yeps-router              | 1.2.0   | ✓      | 44488.0    | 21.99        | 7.93          |
| koa                      | 2.14.2  | ✗      | 44093.8    | 22.19        | 7.86          |
| spirit                   | 0.6.1   | ✗      | 42796.0    | 22.87        | 7.63          |
| spirit-router            | 0.5.0   | ✓      | 41757.6    | 23.46        | 7.45          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41009.8    | 23.88        | 7.31          |
| take-five                | 2.0.0   | ✓      | 40760.8    | 24.05        | 14.65         |
| total.js                 | 3.4.13  | ✓      | 40532.8    | 24.17        | 12.41         |
| restify                  | 8.6.1   | ✓      | 38899.8    | 25.21        | 7.01          |
| koa-router               | 12.0.0  | ✓      | 38225.0    | 25.67        | 6.82          |
| hapi                     | 20.3.0  | ✓      | 33667.8    | 29.21        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 32162.8    | 30.60        | 5.74          |
| trpc-router              | 9.27.3  | ✓      | 27676.8    | 35.62        | 6.12          |
| egg.js                   | 3.17.3  | ✓      | 16449.2    | 60.25        | 5.88          |
| express                  | 4.18.2  | ✓      | 13669.0    | 72.62        | 2.44          |
| express-with-middlewares | 4.18.2  | ✓      | 12066.0    | 82.36        | 4.49          |
| fastify-big-json         | 4.19.1  | ✓      | 11964.8    | 83.08        | 137.66        |
| express-route-prefix     | 4.18.2  | ✓      | 11764.5    | 84.50        | 4.35          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

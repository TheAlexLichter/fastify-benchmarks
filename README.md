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
* __Run:__ Mon Aug 04 2025 03:25:52 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67454.0    | 14.32        | 12.03         |
| polkadot                 | 1.0.0   | ✗      | 61948.8    | 15.66        | 11.05         |
| bare                     | 10.13.0 | ✗      | 60208.0    | 16.11        | 10.74         |
| h3                       | 0.8.6   | ✗      | 58620.0    | 16.56        | 9.62          |
| h3-router                | 0.8.6   | ✓      | 58488.0    | 16.60        | 9.59          |
| foxify                   | 0.10.20 | ✓      | 56092.0    | 17.33        | 9.20          |
| restana                  | 4.9.9   | ✓      | 55903.2    | 17.39        | 9.97          |
| polka                    | 0.5.2   | ✓      | 55087.2    | 17.65        | 9.82          |
| connect                  | 3.7.0   | ✗      | 54822.4    | 17.75        | 9.78          |
| fastify                  | 4.29.1  | ✓      | 53716.8    | 18.12        | 9.63          |
| yeps                     | 1.1.1   | ✗      | 52988.8    | 18.37        | 9.45          |
| micro                    | 9.4.1   | ✗      | 52984.0    | 18.38        | 9.45          |
| server-base-router       | 7.1.32  | ✓      | 51795.2    | 18.81        | 9.24          |
| server-base              | 7.1.32  | ✗      | 51148.8    | 19.06        | 9.12          |
| connect-router           | 1.3.8   | ✓      | 49897.6    | 19.54        | 8.90          |
| micro-route              | 2.5.0   | ✓      | 47833.6    | 20.41        | 8.53          |
| trek-engine              | 1.0.5   | ✗      | 46085.6    | 21.20        | 7.56          |
| vapr                     | 0.6.0   | ✓      | 45789.6    | 21.34        | 7.51          |
| trek-router              | 1.2.0   | ✓      | 45464.8    | 21.49        | 7.46          |
| yeps-router              | 1.2.0   | ✓      | 43610.4    | 22.44        | 7.78          |
| koa                      | 2.16.2  | ✗      | 40787.8    | 24.02        | 7.27          |
| spirit                   | 0.6.1   | ✗      | 38246.6    | 25.65        | 6.82          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37947.8    | 25.85        | 6.77          |
| total.js                 | 3.4.13  | ✓      | 37942.2    | 25.85        | 11.62         |
| spirit-router            | 0.5.0   | ✓      | 37573.8    | 26.12        | 6.70          |
| restify                  | 8.6.1   | ✓      | 37474.6    | 26.18        | 6.75          |
| take-five                | 2.0.0   | ✓      | 37448.2    | 26.21        | 13.46         |
| koa-router               | 12.0.1  | ✓      | 35233.4    | 27.89        | 6.28          |
| hapi                     | 20.3.0  | ✓      | 31943.6    | 30.81        | 5.70          |
| microrouter              | 3.1.3   | ✓      | 30983.2    | 31.78        | 5.53          |
| trpc-router              | 9.27.4  | ✓      | 26984.8    | 36.55        | 5.97          |
| egg.js                   | 3.31.0  | ✓      | 17257.4    | 57.43        | 6.17          |
| express                  | 4.21.2  | ✓      | 13174.6    | 75.37        | 2.35          |
| fastify-big-json         | 4.29.1  | ✓      | 12620.8    | 78.69        | 145.21        |
| express-with-middlewares | 4.21.2  | ✓      | 12359.4    | 80.34        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 10829.4    | 91.76        | 4.01          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

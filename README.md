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
* __Run:__ Mon Oct 07 2024 02:41:19 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 70609.6    | 13.68        | 12.59         |
| polkadot                 | 1.0.0   | ✗      | 67112.8    | 14.41        | 11.97         |
| h3-router                | 0.8.6   | ✓      | 63829.6    | 15.17        | 10.47         |
| h3                       | 0.8.6   | ✗      | 62477.6    | 15.50        | 10.25         |
| restana                  | 4.9.9   | ✓      | 62117.6    | 15.59        | 11.08         |
| bare                     | 10.13.0 | ✗      | 59881.6    | 16.20        | 10.68         |
| connect                  | 3.7.0   | ✗      | 58357.8    | 16.64        | 10.41         |
| polka                    | 0.5.2   | ✓      | 57732.0    | 16.83        | 10.29         |
| fastify                  | 4.28.1  | ✓      | 57553.6    | 16.88        | 10.32         |
| foxify                   | 0.10.20 | ✓      | 57464.0    | 16.90        | 9.43          |
| micro                    | 9.4.1   | ✗      | 56092.8    | 17.33        | 10.00         |
| server-base              | 7.1.32  | ✗      | 55792.8    | 17.42        | 9.95          |
| server-base-router       | 7.1.32  | ✓      | 55410.4    | 17.54        | 9.88          |
| yeps                     | 1.1.1   | ✗      | 51416.8    | 18.96        | 9.17          |
| connect-router           | 1.3.8   | ✓      | 51302.4    | 19.00        | 9.15          |
| micro-route              | 2.5.0   | ✓      | 50576.0    | 19.27        | 9.02          |
| trek-router              | 1.2.0   | ✓      | 47091.2    | 20.73        | 7.72          |
| trek-engine              | 1.0.5   | ✗      | 46004.8    | 21.24        | 7.55          |
| vapr                     | 0.6.0   | ✓      | 45804.0    | 21.34        | 7.51          |
| spirit-router            | 0.5.0   | ✓      | 44534.4    | 21.97        | 7.94          |
| koa                      | 2.15.3  | ✗      | 43318.4    | 22.58        | 7.73          |
| spirit                   | 0.6.1   | ✗      | 43060.0    | 22.78        | 7.68          |
| yeps-router              | 1.2.0   | ✓      | 42491.2    | 23.03        | 7.58          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40358.2    | 24.28        | 7.20          |
| total.js                 | 3.4.13  | ✓      | 39704.0    | 24.69        | 12.16         |
| take-five                | 2.0.0   | ✓      | 39490.6    | 24.84        | 14.20         |
| restify                  | 8.6.1   | ✓      | 39375.0    | 24.91        | 7.10          |
| koa-router               | 12.0.1  | ✓      | 38068.6    | 25.77        | 6.79          |
| hapi                     | 20.3.0  | ✓      | 34240.4    | 28.70        | 6.11          |
| microrouter              | 3.1.3   | ✓      | 32453.6    | 30.30        | 5.79          |
| trpc-router              | 9.27.4  | ✓      | 26910.8    | 36.64        | 5.95          |
| egg.js                   | 3.28.0  | ✓      | 17506.2    | 56.61        | 6.26          |
| express                  | 4.21.0  | ✓      | 13695.2    | 72.45        | 2.44          |
| fastify-big-json         | 4.28.1  | ✓      | 12519.0    | 79.33        | 144.04        |
| express-with-middlewares | 4.21.0  | ✓      | 12451.8    | 79.77        | 4.63          |
| express-route-prefix     | 4.21.0  | ✓      | 10800.8    | 92.00        | 4.00          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

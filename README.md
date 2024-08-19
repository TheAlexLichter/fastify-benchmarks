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
* __Run:__ Mon Aug 19 2024 02:29:18 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68134.8    | 14.19        | 12.15         |
| polkadot                 | 1.0.0   | ✗      | 65427.6    | 14.78        | 11.67         |
| h3-router                | 0.8.6   | ✓      | 59915.2    | 16.19        | 9.83          |
| h3                       | 0.8.6   | ✗      | 59689.6    | 16.27        | 9.79          |
| bare                     | 10.13.0 | ✗      | 59480.0    | 16.31        | 10.61         |
| foxify                   | 0.10.20 | ✓      | 58639.2    | 16.56        | 9.62          |
| restana                  | 4.9.9   | ✓      | 58149.6    | 16.68        | 10.37         |
| polka                    | 0.5.2   | ✓      | 57172.0    | 16.99        | 10.20         |
| micro                    | 9.4.1   | ✗      | 55892.0    | 17.40        | 9.97          |
| server-base-router       | 7.1.32  | ✓      | 55393.6    | 17.56        | 9.88          |
| connect                  | 3.7.0   | ✗      | 54653.6    | 17.80        | 9.75          |
| fastify                  | 4.28.1  | ✓      | 54337.6    | 17.91        | 9.74          |
| server-base              | 7.1.32  | ✗      | 53690.4    | 18.13        | 9.58          |
| yeps                     | 1.1.1   | ✗      | 52192.0    | 18.66        | 9.31          |
| connect-router           | 1.3.8   | ✓      | 50330.4    | 19.38        | 8.98          |
| micro-route              | 2.5.0   | ✓      | 49008.0    | 19.90        | 8.74          |
| trek-engine              | 1.0.5   | ✗      | 47750.4    | 20.45        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 47219.2    | 20.68        | 7.75          |
| vapr                     | 0.6.0   | ✓      | 45916.8    | 21.28        | 7.53          |
| yeps-router              | 1.2.0   | ✓      | 43824.0    | 22.31        | 7.82          |
| koa                      | 2.15.3  | ✗      | 42070.4    | 23.27        | 7.50          |
| spirit                   | 0.6.1   | ✗      | 41975.2    | 23.31        | 7.49          |
| spirit-router            | 0.5.0   | ✓      | 41410.4    | 23.64        | 7.39          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39255.0    | 24.97        | 7.00          |
| total.js                 | 3.4.13  | ✓      | 38453.6    | 25.50        | 11.77         |
| take-five                | 2.0.0   | ✓      | 38308.6    | 25.60        | 13.77         |
| restify                  | 8.6.1   | ✓      | 38217.8    | 25.66        | 6.89          |
| koa-router               | 12.0.1  | ✓      | 36357.4    | 27.00        | 6.48          |
| hapi                     | 20.3.0  | ✓      | 32538.4    | 30.23        | 5.80          |
| microrouter              | 3.1.3   | ✓      | 30987.8    | 31.77        | 5.53          |
| trpc-router              | 9.27.4  | ✓      | 25852.4    | 38.17        | 5.72          |
| egg.js                   | 3.27.1  | ✓      | 17064.1    | 58.08        | 6.10          |
| express                  | 4.19.2  | ✓      | 13478.0    | 73.64        | 2.40          |
| express-with-middlewares | 4.19.2  | ✓      | 12596.8    | 78.83        | 4.69          |
| fastify-big-json         | 4.28.1  | ✓      | 12595.6    | 78.82        | 144.92        |
| express-route-prefix     | 4.19.2  | ✓      | 10613.0    | 93.64        | 3.93          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

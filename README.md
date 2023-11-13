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
* __Run:__ Mon Nov 13 2023 02:11:13 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 55693.6    | 17.47        | 9.93          |
| 0http                    | 3.5.2   | ✓      | 52312.8    | 18.63        | 9.33          |
| h3-router                | 0.8.6   | ✓      | 50440.8    | 19.35        | 8.27          |
| h3                       | 0.8.6   | ✗      | 48614.4    | 20.08        | 7.97          |
| polka                    | 0.5.2   | ✓      | 48037.6    | 20.32        | 8.57          |
| foxify                   | 0.10.20 | ✓      | 46890.4    | 20.84        | 7.69          |
| bare                     | 10.13.0 | ✗      | 46888.8    | 20.85        | 8.36          |
| fastify                  | 4.24.3  | ✓      | 46079.2    | 21.21        | 8.26          |
| connect                  | 3.7.0   | ✗      | 46044.0    | 21.22        | 8.21          |
| restana                  | 4.9.7   | ✓      | 45156.8    | 21.65        | 8.05          |
| server-base              | 7.1.32  | ✗      | 45035.2    | 21.71        | 8.03          |
| micro                    | 9.4.1   | ✗      | 44929.6    | 21.76        | 8.01          |
| server-base-router       | 7.1.32  | ✓      | 43928.8    | 22.28        | 7.83          |
| connect-router           | 1.3.8   | ✓      | 42042.4    | 23.29        | 7.50          |
| micro-route              | 2.5.0   | ✓      | 41706.6    | 23.48        | 7.44          |
| yeps                     | 1.1.1   | ✗      | 41244.6    | 23.75        | 7.36          |
| trek-engine              | 1.0.5   | ✗      | 39774.6    | 24.64        | 6.52          |
| spirit                   | 0.6.1   | ✗      | 37915.4    | 25.89        | 6.76          |
| trek-router              | 1.2.0   | ✓      | 37756.0    | 25.98        | 6.19          |
| spirit-router            | 0.5.0   | ✓      | 36089.0    | 27.23        | 6.44          |
| yeps-router              | 1.2.0   | ✓      | 36060.4    | 27.24        | 6.43          |
| vapr                     | 0.6.0   | ✓      | 35248.2    | 27.88        | 5.78          |
| koa                      | 2.14.2  | ✗      | 34934.8    | 28.13        | 6.23          |
| take-five                | 2.0.0   | ✓      | 33064.4    | 29.74        | 11.89         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 32700.2    | 30.08        | 5.83          |
| restify                  | 8.6.1   | ✓      | 32298.8    | 30.47        | 5.82          |
| total.js                 | 3.4.13  | ✓      | 31699.4    | 31.05        | 9.70          |
| koa-router               | 12.0.1  | ✓      | 30700.2    | 32.07        | 5.47          |
| hapi                     | 20.3.0  | ✓      | 27144.4    | 36.34        | 4.84          |
| microrouter              | 3.1.3   | ✓      | 24914.8    | 39.63        | 4.44          |
| trpc-router              | 9.27.3  | ✓      | 21597.6    | 45.78        | 4.78          |
| egg.js                   | 3.17.5  | ✓      | 14951.4    | 66.37        | 5.35          |
| express                  | 4.18.2  | ✓      | 11446.0    | 86.81        | 2.04          |
| fastify-big-json         | 4.24.3  | ✓      | 10603.0    | 93.74        | 121.99        |
| express-with-middlewares | 4.18.2  | ✓      | 9616.5     | 103.41       | 3.58          |
| express-route-prefix     | 4.18.2  | ✓      | 9291.8     | 107.01       | 3.44          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jul 17 2023 02:54:25 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 56748.8    | 17.13        | 10.12         |
| connect                  | 3.7.0   | ✗      | 55161.6    | 17.63        | 9.84          |
| micro                    | 9.4.1   | ✗      | 55038.4    | 17.67        | 9.81          |
| polkadot                 | 1.0.0   | ✗      | 54961.6    | 17.71        | 9.80          |
| polka                    | 0.5.2   | ✓      | 54952.0    | 17.70        | 9.80          |
| 0http                    | 3.5.2   | ✓      | 54802.4    | 17.77        | 9.77          |
| foxify                   | 0.10.20 | ✓      | 54052.0    | 18.00        | 8.87          |
| h3                       | 0.8.6   | ✗      | 53136.0    | 18.32        | 8.72          |
| h3-router                | 0.8.6   | ✓      | 52734.4    | 18.47        | 8.65          |
| fastify                  | 4.19.2  | ✓      | 52362.4    | 18.61        | 9.39          |
| server-base              | 7.1.32  | ✗      | 50669.6    | 19.24        | 9.04          |
| yeps                     | 1.1.1   | ✗      | 49928.8    | 19.53        | 8.90          |
| server-base-router       | 7.1.32  | ✓      | 49585.6    | 19.67        | 8.84          |
| restana                  | 4.9.7   | ✓      | 48697.6    | 19.99        | 8.68          |
| micro-route              | 2.5.0   | ✓      | 47696.8    | 20.48        | 8.51          |
| connect-router           | 1.3.8   | ✓      | 46885.6    | 20.84        | 8.36          |
| trek-engine              | 1.0.5   | ✗      | 45338.6    | 21.56        | 7.44          |
| trek-router              | 1.2.0   | ✓      | 45164.8    | 21.65        | 7.41          |
| vapr                     | 0.6.0   | ✓      | 43337.6    | 22.57        | 7.11          |
| koa                      | 2.14.2  | ✗      | 40581.8    | 24.14        | 7.24          |
| yeps-router              | 1.2.0   | ✓      | 40430.2    | 24.24        | 7.21          |
| spirit                   | 0.6.1   | ✗      | 37908.0    | 25.90        | 6.76          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36646.6    | 26.80        | 6.54          |
| spirit-router            | 0.5.0   | ✓      | 36639.8    | 26.81        | 6.53          |
| total.js                 | 3.4.13  | ✓      | 36560.6    | 26.86        | 11.19         |
| take-five                | 2.0.0   | ✓      | 36460.6    | 26.92        | 13.11         |
| restify                  | 8.6.1   | ✓      | 35467.0    | 27.70        | 6.39          |
| koa-router               | 12.0.0  | ✓      | 32362.0    | 30.40        | 5.77          |
| hapi                     | 20.3.0  | ✓      | 28827.6    | 34.18        | 5.14          |
| microrouter              | 3.1.3   | ✓      | 28136.4    | 35.04        | 5.02          |
| trpc-router              | 9.27.3  | ✓      | 24463.2    | 40.36        | 5.41          |
| egg.js                   | 3.17.3  | ✓      | 14484.0    | 68.54        | 5.18          |
| express                  | 4.18.2  | ✓      | 11853.0    | 83.82        | 2.11          |
| express-with-middlewares | 4.18.2  | ✓      | 10278.1    | 96.72        | 3.82          |
| express-route-prefix     | 4.18.2  | ✓      | 9808.4     | 101.46       | 3.63          |
| fastify-big-json         | 4.19.2  | ✓      | 9624.4     | 103.41       | 110.74        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

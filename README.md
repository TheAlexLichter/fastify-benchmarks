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
* __Run:__ Mon Jun 19 2023 02:37:29 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 61968.0    | 15.65        | 11.05         |
| 0http                    | 3.5.2   | ✓      | 58860.8    | 16.49        | 10.50         |
| bare                     | 10.13.0 | ✗      | 58847.2    | 16.50        | 10.49         |
| h3                       | 0.8.6   | ✗      | 58821.6    | 16.50        | 9.65          |
| h3-router                | 0.8.6   | ✓      | 58296.0    | 16.66        | 9.56          |
| foxify                   | 0.10.20 | ✓      | 57570.4    | 16.87        | 9.44          |
| polka                    | 0.5.2   | ✓      | 56809.6    | 17.11        | 10.13         |
| fastify                  | 4.18.0  | ✓      | 56771.2    | 17.12        | 10.18         |
| server-base-router       | 7.1.32  | ✓      | 54611.2    | 17.81        | 9.74          |
| server-base              | 7.1.32  | ✗      | 54503.2    | 17.85        | 9.72          |
| micro                    | 9.4.1   | ✗      | 54494.4    | 17.85        | 9.72          |
| restana                  | 4.9.7   | ✓      | 54359.2    | 17.88        | 9.69          |
| connect                  | 3.7.0   | ✗      | 54152.6    | 17.98        | 9.66          |
| yeps                     | 1.1.1   | ✗      | 54137.6    | 17.98        | 9.65          |
| connect-router           | 1.3.8   | ✓      | 51246.4    | 19.02        | 9.14          |
| micro-route              | 2.5.0   | ✓      | 49799.2    | 19.59        | 8.88          |
| trek-engine              | 1.0.5   | ✗      | 48078.4    | 20.30        | 7.89          |
| vapr                     | 0.6.0   | ✓      | 47627.2    | 20.50        | 7.81          |
| trek-router              | 1.2.0   | ✓      | 47246.6    | 20.67        | 7.75          |
| yeps-router              | 1.2.0   | ✓      | 43836.8    | 22.31        | 7.82          |
| koa                      | 2.14.2  | ✗      | 43566.4    | 22.46        | 7.77          |
| spirit                   | 0.6.1   | ✗      | 42405.6    | 23.09        | 7.56          |
| spirit-router            | 0.5.0   | ✓      | 41109.6    | 23.82        | 7.33          |
| take-five                | 2.0.0   | ✓      | 41001.8    | 23.89        | 14.74         |
| total.js                 | 3.4.13  | ✓      | 39967.0    | 24.52        | 12.23         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39930.6    | 24.55        | 7.12          |
| restify                  | 8.6.1   | ✓      | 38420.8    | 25.53        | 6.92          |
| koa-router               | 12.0.0  | ✓      | 36859.8    | 26.64        | 6.57          |
| hapi                     | 20.3.0  | ✓      | 32839.0    | 29.95        | 5.86          |
| microrouter              | 3.1.3   | ✓      | 31893.6    | 30.85        | 5.69          |
| trpc-router              | 9.27.3  | ✓      | 27501.6    | 35.86        | 6.08          |
| egg.js                   | 3.16.1  | ✓      | 16270.7    | 60.93        | 5.82          |
| express                  | 4.18.2  | ✓      | 13615.8    | 72.91        | 2.43          |
| express-with-middlewares | 4.18.2  | ✓      | 11898.4    | 83.47        | 4.43          |
| express-route-prefix     | 4.18.2  | ✓      | 11587.6    | 85.68        | 4.29          |
| fastify-big-json         | 4.18.0  | ✓      | 11464.6    | 86.74        | 131.92        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

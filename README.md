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
* __Run:__ Mon Dec 18 2023 02:12:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67436.0    | 14.34        | 12.03         |
| h3                       | 0.8.6   | ✗      | 64781.6    | 14.95        | 10.63         |
| 0http                    | 3.5.2   | ✓      | 64380.8    | 15.04        | 11.48         |
| h3-router                | 0.8.6   | ✓      | 62540.0    | 15.48        | 10.26         |
| bare                     | 10.13.0 | ✗      | 59924.0    | 16.18        | 10.69         |
| foxify                   | 0.10.20 | ✓      | 59000.0    | 16.45        | 9.68          |
| polka                    | 0.5.2   | ✓      | 58536.8    | 16.58        | 10.44         |
| connect                  | 3.7.0   | ✗      | 55744.0    | 17.44        | 9.94          |
| fastify                  | 4.25.1  | ✓      | 55728.8    | 17.45        | 9.99          |
| restana                  | 4.9.7   | ✓      | 55260.0    | 17.60        | 9.85          |
| micro                    | 9.4.1   | ✗      | 54808.8    | 17.74        | 9.77          |
| server-base-router       | 7.1.32  | ✓      | 54311.2    | 17.92        | 9.69          |
| server-base              | 7.1.32  | ✗      | 54104.8    | 17.99        | 9.65          |
| yeps                     | 1.1.1   | ✗      | 51344.8    | 18.98        | 9.16          |
| micro-route              | 2.5.0   | ✓      | 49904.0    | 19.53        | 8.90          |
| trek-engine              | 1.0.5   | ✗      | 49410.4    | 19.74        | 8.10          |
| connect-router           | 1.3.8   | ✓      | 49139.2    | 19.84        | 8.76          |
| trek-router              | 1.2.0   | ✓      | 47953.6    | 20.35        | 7.87          |
| vapr                     | 0.6.0   | ✓      | 46181.6    | 21.15        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 44457.6    | 22.04        | 7.93          |
| yeps-router              | 1.2.0   | ✓      | 43956.8    | 22.26        | 7.84          |
| spirit-router            | 0.5.0   | ✓      | 42788.0    | 22.85        | 7.63          |
| koa                      | 2.14.2  | ✗      | 41572.0    | 23.55        | 7.41          |
| total.js                 | 3.4.13  | ✓      | 40303.2    | 24.32        | 12.34         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39426.2    | 24.86        | 7.03          |
| restify                  | 8.6.1   | ✓      | 39281.8    | 24.96        | 7.08          |
| take-five                | 2.0.0   | ✓      | 38654.6    | 25.38        | 13.90         |
| koa-router               | 12.0.1  | ✓      | 36892.2    | 26.60        | 6.58          |
| hapi                     | 20.3.0  | ✓      | 34547.4    | 28.45        | 6.16          |
| microrouter              | 3.1.3   | ✓      | 32232.2    | 30.53        | 5.75          |
| trpc-router              | 9.27.3  | ✓      | 26533.2    | 37.19        | 5.87          |
| egg.js                   | 3.17.5  | ✓      | 17765.9    | 55.76        | 6.35          |
| express                  | 4.18.2  | ✓      | 13375.4    | 74.22        | 2.39          |
| fastify-big-json         | 4.25.1  | ✓      | 12809.8    | 77.51        | 147.39        |
| express-with-middlewares | 4.18.2  | ✓      | 12489.6    | 79.52        | 4.65          |
| express-route-prefix     | 4.18.2  | ✓      | 10985.4    | 90.46        | 4.06          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

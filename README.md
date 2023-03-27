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
* __Run:__ Mon Mar 27 2023 02:25:51 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 62284.8    | 15.57        | 11.11         |
| polkadot                 | 1.0.0   | ✗      | 62071.2    | 15.63        | 11.07         |
| 0http                    | 3.5.1   | ✓      | 60517.6    | 16.05        | 10.79         |
| h3                       | 0.8.6   | ✗      | 60357.6    | 16.06        | 9.90          |
| h3-router                | 0.8.6   | ✓      | 59832.0    | 16.21        | 9.81          |
| fastify                  | 4.15.0  | ✓      | 59532.8    | 16.30        | 10.67         |
| polka                    | 0.5.2   | ✓      | 59393.6    | 16.35        | 10.59         |
| foxify                   | 0.10.20 | ✓      | 58972.0    | 16.46        | 9.67          |
| micro                    | 9.4.1   | ✗      | 57956.8    | 16.76        | 10.34         |
| server-base              | 7.1.32  | ✗      | 57068.0    | 17.03        | 10.18         |
| connect                  | 3.7.0   | ✗      | 56848.8    | 17.09        | 10.14         |
| server-base-router       | 7.1.32  | ✓      | 54891.2    | 17.71        | 9.79          |
| yeps                     | 1.1.1   | ✗      | 54491.2    | 17.86        | 9.72          |
| restana                  | 4.9.7   | ✓      | 54201.6    | 18.03        | 9.67          |
| connect-router           | 1.3.8   | ✓      | 53030.4    | 18.37        | 9.46          |
| micro-route              | 2.5.0   | ✓      | 52032.8    | 18.72        | 9.28          |
| trek-router              | 1.2.0   | ✓      | 49768.0    | 19.60        | 8.16          |
| trek-engine              | 1.0.5   | ✗      | 49258.4    | 19.80        | 8.08          |
| vapr                     | 0.6.0   | ✓      | 48884.0    | 19.97        | 8.02          |
| yeps-router              | 1.2.0   | ✓      | 44957.6    | 21.75        | 8.02          |
| koa                      | 2.14.1  | ✗      | 44781.6    | 21.84        | 7.99          |
| spirit                   | 0.6.1   | ✗      | 43989.6    | 22.24        | 7.84          |
| spirit-router            | 0.5.0   | ✓      | 42643.2    | 22.97        | 7.61          |
| take-five                | 2.0.0   | ✓      | 41445.0    | 23.64        | 14.90         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41176.6    | 23.78        | 7.34          |
| total.js                 | 3.4.13  | ✓      | 40151.2    | 24.41        | 12.29         |
| restify                  | 8.6.1   | ✓      | 39659.0    | 24.71        | 7.15          |
| koa-router               | 12.0.0  | ✓      | 37959.0    | 25.85        | 6.77          |
| hapi                     | 20.3.0  | ✓      | 33973.4    | 28.92        | 6.06          |
| microrouter              | 3.1.3   | ✓      | 32704.8    | 30.08        | 5.83          |
| trpc-router              | 9.27.3  | ✓      | 27875.2    | 35.37        | 6.17          |
| egg.js                   | 3.15.0  | ✓      | 16598.3    | 59.74        | 5.94          |
| express                  | 4.18.2  | ✓      | 13813.8    | 71.86        | 2.46          |
| fastify-big-json         | 4.15.0  | ✓      | 12009.0    | 82.76        | 138.17        |
| express-with-middlewares | 4.18.2  | ✓      | 11992.4    | 82.82        | 4.46          |
| express-route-prefix     | 4.18.2  | ✓      | 11632.9    | 85.39        | 4.30          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

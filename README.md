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
* __Run:__ Mon Sep 01 2025 03:10:41 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69666.0    | 13.85        | 12.42         |
| polkadot                 | 1.0.0   | ✗      | 68346.8    | 14.15        | 12.19         |
| h3-router                | 0.8.6   | ✓      | 67010.8    | 14.43        | 10.99         |
| h3                       | 0.8.6   | ✗      | 64006.0    | 15.14        | 10.50         |
| restana                  | 4.9.9   | ✓      | 61976.0    | 15.62        | 11.05         |
| bare                     | 10.13.0 | ✗      | 61929.6    | 15.67        | 11.04         |
| foxify                   | 0.10.20 | ✓      | 60180.8    | 16.11        | 9.87          |
| polka                    | 0.5.2   | ✓      | 59743.2    | 16.24        | 10.65         |
| connect                  | 3.7.0   | ✗      | 58555.2    | 16.57        | 10.44         |
| micro                    | 9.4.1   | ✗      | 57821.6    | 16.80        | 10.31         |
| server-base-router       | 7.1.32  | ✓      | 55687.2    | 17.46        | 9.93          |
| server-base              | 7.1.32  | ✗      | 55509.6    | 17.51        | 9.90          |
| fastify                  | 4.29.1  | ✓      | 54573.6    | 17.83        | 9.78          |
| yeps                     | 1.1.1   | ✗      | 52900.8    | 18.40        | 9.43          |
| micro-route              | 2.5.0   | ✓      | 51428.8    | 18.95        | 9.17          |
| connect-router           | 1.3.8   | ✓      | 50805.6    | 19.19        | 9.06          |
| trek-engine              | 1.0.5   | ✗      | 48876.0    | 19.97        | 8.02          |
| trek-router              | 1.2.0   | ✓      | 48056.0    | 20.32        | 7.88          |
| vapr                     | 0.6.0   | ✓      | 46560.0    | 20.97        | 7.64          |
| spirit                   | 0.6.1   | ✗      | 45654.4    | 21.39        | 8.14          |
| yeps-router              | 1.2.0   | ✓      | 44680.0    | 21.90        | 7.97          |
| spirit-router            | 0.5.0   | ✓      | 43822.4    | 22.31        | 7.82          |
| koa                      | 2.16.2  | ✗      | 42560.8    | 22.99        | 7.59          |
| total.js                 | 3.4.13  | ✓      | 40905.6    | 23.94        | 12.52         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39864.2    | 24.59        | 7.11          |
| restify                  | 8.6.1   | ✓      | 39279.2    | 24.97        | 7.08          |
| take-five                | 2.0.0   | ✓      | 39122.6    | 25.06        | 14.07         |
| koa-router               | 12.0.1  | ✓      | 37346.2    | 26.28        | 6.66          |
| hapi                     | 20.3.0  | ✓      | 34660.2    | 28.34        | 6.18          |
| microrouter              | 3.1.3   | ✓      | 31960.2    | 30.80        | 5.70          |
| trpc-router              | 9.27.4  | ✓      | 28016.0    | 35.19        | 6.20          |
| egg.js                   | 3.31.0  | ✓      | 17622.8    | 56.21        | 6.30          |
| express                  | 4.21.2  | ✓      | 13668.2    | 72.59        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12591.8    | 78.88        | 144.87        |
| express-with-middlewares | 4.21.2  | ✓      | 12368.2    | 80.30        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 11089.6    | 89.60        | 4.10          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

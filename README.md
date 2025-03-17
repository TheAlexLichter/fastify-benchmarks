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
* __Run:__ Mon Mar 17 2025 02:47:08 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68192.4    | 14.16        | 12.16         |
| polkadot                 | 1.0.0   | ✗      | 68161.2    | 14.18        | 12.16         |
| h3                       | 0.8.6   | ✗      | 64611.6    | 14.99        | 10.60         |
| h3-router                | 0.8.6   | ✓      | 63414.8    | 15.27        | 10.40         |
| restana                  | 4.9.9   | ✓      | 61374.4    | 15.79        | 10.95         |
| bare                     | 10.13.0 | ✗      | 60999.2    | 15.91        | 10.88         |
| polka                    | 0.5.2   | ✓      | 60279.2    | 16.09        | 10.75         |
| foxify                   | 0.10.20 | ✓      | 60066.4    | 16.15        | 9.85          |
| connect                  | 3.7.0   | ✗      | 58596.8    | 16.57        | 10.45         |
| micro                    | 9.4.1   | ✗      | 58435.2    | 16.61        | 10.42         |
| fastify                  | 4.29.0  | ✓      | 57465.6    | 16.90        | 10.30         |
| server-base              | 7.1.32  | ✗      | 57044.8    | 17.04        | 10.17         |
| server-base-router       | 7.1.32  | ✓      | 55397.6    | 17.55        | 9.88          |
| yeps                     | 1.1.1   | ✗      | 54526.4    | 17.84        | 9.72          |
| connect-router           | 1.3.8   | ✓      | 51180.8    | 19.03        | 9.13          |
| micro-route              | 2.5.0   | ✓      | 51052.8    | 19.09        | 9.11          |
| trek-engine              | 1.0.5   | ✗      | 49678.4    | 19.63        | 8.15          |
| trek-router              | 1.2.0   | ✓      | 48899.2    | 19.96        | 8.02          |
| vapr                     | 0.6.0   | ✓      | 47358.4    | 20.62        | 7.77          |
| spirit                   | 0.6.1   | ✗      | 44851.2    | 21.83        | 8.00          |
| yeps-router              | 1.2.0   | ✓      | 44797.6    | 21.82        | 7.99          |
| koa                      | 2.16.0  | ✗      | 43276.8    | 22.61        | 7.72          |
| spirit-router            | 0.5.0   | ✓      | 42703.2    | 22.91        | 7.62          |
| total.js                 | 3.4.13  | ✓      | 40460.8    | 24.21        | 12.39         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40386.6    | 24.26        | 7.20          |
| restify                  | 8.6.1   | ✓      | 40293.6    | 24.32        | 7.26          |
| take-five                | 2.0.0   | ✓      | 39197.0    | 25.01        | 14.09         |
| koa-router               | 12.0.1  | ✓      | 37582.6    | 26.11        | 6.70          |
| hapi                     | 20.3.0  | ✓      | 34359.8    | 28.61        | 6.13          |
| microrouter              | 3.1.3   | ✓      | 32931.8    | 29.85        | 5.87          |
| trpc-router              | 9.27.4  | ✓      | 28290.8    | 34.84        | 6.26          |
| egg.js                   | 3.30.1  | ✓      | 17523.1    | 56.55        | 6.27          |
| express                  | 4.21.2  | ✓      | 13840.2    | 71.71        | 2.47          |
| fastify-big-json         | 4.29.0  | ✓      | 12743.4    | 77.92        | 146.62        |
| express-with-middlewares | 4.21.2  | ✓      | 12440.8    | 79.82        | 4.63          |
| express-route-prefix     | 4.21.2  | ✓      | 11056.8    | 89.87        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

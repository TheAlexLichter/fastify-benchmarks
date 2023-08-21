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
* __Run:__ Mon Aug 21 2023 02:04:06 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 53638.4    | 18.15        | 9.57          |
| connect                  | 3.7.0   | ✗      | 53153.6    | 18.32        | 9.48          |
| foxify                   | 0.10.20 | ✓      | 53148.0    | 18.32        | 8.72          |
| micro                    | 9.4.1   | ✗      | 52581.4    | 18.52        | 9.38          |
| polkadot                 | 1.0.0   | ✗      | 52254.4    | 18.65        | 9.32          |
| fastify                  | 4.21.0  | ✓      | 51568.0    | 18.89        | 9.25          |
| polka                    | 0.5.2   | ✓      | 51461.6    | 18.94        | 9.18          |
| 0http                    | 3.5.2   | ✓      | 50058.4    | 19.48        | 8.93          |
| server-base-router       | 7.1.32  | ✓      | 49387.2    | 19.75        | 8.81          |
| h3                       | 0.8.6   | ✗      | 49321.6    | 19.78        | 8.09          |
| server-base              | 7.1.32  | ✗      | 49283.2    | 19.80        | 8.79          |
| h3-router                | 0.8.6   | ✓      | 48523.2    | 20.11        | 7.96          |
| yeps                     | 1.1.1   | ✗      | 48132.0    | 20.28        | 8.58          |
| connect-router           | 1.3.8   | ✓      | 47324.8    | 20.63        | 8.44          |
| restana                  | 4.9.7   | ✓      | 45065.6    | 21.70        | 8.04          |
| micro-route              | 2.5.0   | ✓      | 45019.2    | 21.71        | 8.03          |
| trek-engine              | 1.0.5   | ✗      | 44478.2    | 21.99        | 7.30          |
| trek-router              | 1.2.0   | ✓      | 42885.0    | 22.82        | 7.03          |
| vapr                     | 0.6.0   | ✓      | 40627.4    | 24.11        | 6.66          |
| yeps-router              | 1.2.0   | ✓      | 39991.8    | 24.51        | 7.13          |
| koa                      | 2.14.2  | ✗      | 37946.2    | 25.85        | 6.77          |
| spirit                   | 0.6.1   | ✗      | 37801.0    | 25.96        | 6.74          |
| take-five                | 2.0.0   | ✓      | 36653.0    | 26.79        | 13.18         |
| total.js                 | 3.4.13  | ✓      | 35911.0    | 27.35        | 10.99         |
| spirit-router            | 0.5.0   | ✓      | 35796.8    | 27.45        | 6.38          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 35534.2    | 27.64        | 6.34          |
| restify                  | 8.6.1   | ✓      | 34920.2    | 28.14        | 6.29          |
| koa-router               | 12.0.0  | ✓      | 32911.8    | 29.88        | 5.87          |
| hapi                     | 20.3.0  | ✓      | 30020.8    | 32.81        | 5.35          |
| microrouter              | 3.1.3   | ✓      | 27496.0    | 35.87        | 4.90          |
| trpc-router              | 9.27.3  | ✓      | 24242.4    | 40.74        | 5.36          |
| egg.js                   | 3.17.4  | ✓      | 14486.8    | 68.50        | 5.18          |
| express                  | 4.18.2  | ✓      | 11767.0    | 84.47        | 2.10          |
| express-with-middlewares | 4.18.2  | ✓      | 10248.3    | 97.01        | 3.81          |
| express-route-prefix     | 4.18.2  | ✓      | 10171.0    | 97.73        | 3.76          |
| fastify-big-json         | 4.21.0  | ✓      | 9544.3     | 104.29       | 109.81        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

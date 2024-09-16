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
* __Run:__ Mon Sep 16 2024 02:39:22 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67749.2    | 14.26        | 12.08         |
| h3                       | 0.8.6   | ✗      | 66122.0    | 14.62        | 10.85         |
| polkadot                 | 1.0.0   | ✗      | 64724.0    | 14.94        | 11.54         |
| h3-router                | 0.8.6   | ✓      | 62968.0    | 15.39        | 10.33         |
| restana                  | 4.9.9   | ✓      | 61357.6    | 15.79        | 10.94         |
| bare                     | 10.13.0 | ✗      | 60224.0    | 16.11        | 10.74         |
| foxify                   | 0.10.20 | ✓      | 59116.8    | 16.41        | 9.70          |
| connect                  | 3.7.0   | ✗      | 57638.4    | 16.85        | 10.28         |
| polka                    | 0.5.2   | ✓      | 57371.2    | 16.95        | 10.23         |
| fastify                  | 4.28.1  | ✓      | 56240.0    | 17.29        | 10.08         |
| micro                    | 9.4.1   | ✗      | 55979.2    | 17.37        | 9.98          |
| server-base-router       | 7.1.32  | ✓      | 53668.0    | 18.14        | 9.57          |
| server-base              | 7.1.32  | ✗      | 52738.4    | 18.47        | 9.40          |
| yeps                     | 1.1.1   | ✗      | 52199.2    | 18.65        | 9.31          |
| connect-router           | 1.3.8   | ✓      | 50579.2    | 19.28        | 9.02          |
| micro-route              | 2.5.0   | ✓      | 48004.8    | 20.33        | 8.56          |
| trek-engine              | 1.0.5   | ✗      | 47760.0    | 20.44        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 46785.6    | 20.87        | 7.67          |
| vapr                     | 0.6.0   | ✓      | 45518.4    | 21.46        | 7.47          |
| yeps-router              | 1.2.0   | ✓      | 43992.8    | 22.24        | 7.85          |
| spirit                   | 0.6.1   | ✗      | 43363.2    | 22.52        | 7.73          |
| koa                      | 2.15.3  | ✗      | 42379.2    | 23.09        | 7.56          |
| spirit-router            | 0.5.0   | ✓      | 41595.2    | 23.51        | 7.42          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39941.4    | 24.54        | 7.12          |
| total.js                 | 3.4.13  | ✓      | 39341.6    | 24.92        | 12.04         |
| restify                  | 8.6.1   | ✓      | 39187.0    | 25.03        | 7.06          |
| take-five                | 2.0.0   | ✓      | 37904.6    | 25.89        | 13.63         |
| koa-router               | 12.0.1  | ✓      | 36547.8    | 26.86        | 6.52          |
| hapi                     | 20.3.0  | ✓      | 33440.4    | 29.40        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 30652.8    | 32.11        | 5.47          |
| trpc-router              | 9.27.4  | ✓      | 26344.4    | 37.45        | 5.83          |
| egg.js                   | 3.27.1  | ✓      | 17630.3    | 56.20        | 6.31          |
| express                  | 4.21.0  | ✓      | 13613.6    | 72.91        | 2.43          |
| fastify-big-json         | 4.28.1  | ✓      | 12796.6    | 77.62        | 147.23        |
| express-with-middlewares | 4.21.0  | ✓      | 12600.6    | 78.81        | 4.69          |
| express-route-prefix     | 4.21.0  | ✓      | 10871.0    | 91.41        | 4.02          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

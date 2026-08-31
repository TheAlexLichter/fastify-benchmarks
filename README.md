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
* __Run:__ Mon Aug 31 2026 06:07:08 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 64017.6    | 15.13        | 11.42         |
| 0http                    | 3.5.3   | ✓      | 62388.0    | 15.53        | 11.13         |
| bare                     | 10.13.0 | ✗      | 57376.8    | 16.93        | 10.23         |
| restana                  | 4.9.9   | ✓      | 57194.4    | 16.98        | 10.20         |
| micro                    | 9.4.1   | ✗      | 54852.8    | 17.73        | 9.78          |
| polka                    | 0.5.2   | ✓      | 54720.0    | 17.79        | 9.76          |
| connect                  | 3.7.0   | ✗      | 54456.0    | 17.87        | 9.71          |
| h3                       | 0.8.6   | ✗      | 54180.0    | 17.96        | 8.89          |
| foxify                   | 0.10.20 | ✓      | 53836.8    | 18.08        | 8.83          |
| server-base              | 7.1.32  | ✗      | 52741.6    | 18.46        | 9.41          |
| h3-router                | 0.8.6   | ✓      | 52430.4    | 18.58        | 8.60          |
| server-base-router       | 7.1.32  | ✓      | 52219.2    | 18.65        | 9.31          |
| yeps                     | 1.1.1   | ✗      | 50490.4    | 19.31        | 9.00          |
| fastify                  | 4.29.1  | ✓      | 49624.8    | 19.65        | 8.90          |
| connect-router           | 1.3.8   | ✓      | 48329.6    | 20.20        | 8.62          |
| trek-engine              | 1.0.5   | ✗      | 48225.6    | 20.24        | 7.91          |
| micro-route              | 2.5.0   | ✓      | 47943.2    | 20.36        | 8.55          |
| trek-router              | 1.2.0   | ✓      | 46494.4    | 21.01        | 7.63          |
| vapr                     | 0.6.0   | ✓      | 46040.8    | 21.22        | 7.55          |
| yeps-router              | 1.2.0   | ✓      | 42740.0    | 22.90        | 7.62          |
| spirit-router            | 0.5.0   | ✓      | 40836.8    | 23.99        | 7.28          |
| spirit                   | 0.6.1   | ✗      | 39724.8    | 24.67        | 7.08          |
| total.js                 | 3.4.13  | ✓      | 39411.2    | 24.87        | 12.06         |
| take-five                | 2.0.0   | ✓      | 39012.6    | 25.13        | 14.03         |
| koa                      | 2.16.4  | ✗      | 38533.4    | 25.45        | 6.87          |
| restify                  | 8.6.1   | ✓      | 36994.6    | 26.52        | 6.67          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36355.4    | 27.01        | 6.48          |
| koa-router               | 12.0.1  | ✓      | 34918.8    | 28.13        | 6.23          |
| hapi                     | 20.3.0  | ✓      | 31115.2    | 31.63        | 5.55          |
| microrouter              | 3.1.3   | ✓      | 30731.2    | 32.04        | 5.48          |
| trpc-router              | 9.27.4  | ✓      | 26554.8    | 37.15        | 5.88          |
| egg.js                   | 3.34.0  | ✓      | 16923.0    | 58.55        | 6.05          |
| express                  | 4.22.2  | ✓      | 13214.6    | 75.13        | 2.36          |
| fastify-big-json         | 4.29.1  | ✓      | 11533.2    | 86.16        | 132.69        |
| express-with-middlewares | 4.22.2  | ✓      | 11458.0    | 86.72        | 4.26          |
| express-route-prefix     | 4.22.2  | ✓      | 9891.9     | 100.49       | 3.66          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

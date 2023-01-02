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
* __Node:__ `v14.21.1`
* __Run:__ Mon Jan 02 2023 02:30:47 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 37253.8    | 26.35        | 6.64          |
| micro                    | 9.4.1   | ✗      | 37124.2    | 26.44        | 6.62          |
| h3-router                | 0.8.6   | ✓      | 35709.8    | 27.51        | 5.86          |
| bare                     | 10.13.0 | ✗      | 34693.4    | 28.33        | 6.19          |
| h3                       | 0.8.6   | ✗      | 34675.0    | 28.34        | 5.69          |
| foxify                   | 0.10.20 | ✓      | 34110.4    | 28.82        | 5.59          |
| 0http                    | 3.4.2   | ✓      | 34023.0    | 28.90        | 6.07          |
| connect                  | 3.7.0   | ✗      | 33382.1    | 29.47        | 5.95          |
| polka                    | 0.5.2   | ✓      | 31592.6    | 31.16        | 5.63          |
| fastify                  | 4.11.0  | ✓      | 31377.8    | 31.36        | 5.63          |
| yeps                     | 1.1.1   | ✗      | 30581.4    | 32.19        | 5.45          |
| server-base              | 7.1.32  | ✗      | 29622.8    | 33.26        | 5.28          |
| server-base-router       | 7.1.32  | ✓      | 29530.4    | 33.36        | 5.27          |
| connect-router           | 1.3.7   | ✓      | 29293.0    | 33.65        | 5.22          |
| trek-engine              | 1.0.5   | ✗      | 28869.6    | 34.13        | 4.74          |
| spirit-router            | 0.5.0   | ✓      | 28695.4    | 34.43        | 5.12          |
| micro-route              | 2.5.0   | ✓      | 27582.0    | 35.75        | 4.92          |
| restana                  | 4.9.7   | ✓      | 26642.0    | 37.03        | 4.75          |
| trek-router              | 1.2.0   | ✓      | 25518.5    | 38.69        | 4.19          |
| vapr                     | 0.6.0   | ✓      | 25160.4    | 39.24        | 4.13          |
| koa                      | 2.14.1  | ✗      | 24728.0    | 39.94        | 4.41          |
| yeps-router              | 1.2.0   | ✓      | 24581.2    | 40.17        | 4.38          |
| spirit                   | 0.6.1   | ✗      | 24067.2    | 41.08        | 4.29          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 23550.8    | 41.95        | 4.20          |
| restify                  | 8.6.1   | ✓      | 22842.4    | 43.27        | 4.12          |
| total.js                 | 3.4.13  | ✓      | 22531.2    | 43.87        | 6.90          |
| koa-router               | 12.0.0  | ✓      | 22188.4    | 44.57        | 3.96          |
| take-five                | 2.0.0   | ✓      | 21615.1    | 45.75        | 7.77          |
| hapi                     | 20.2.2  | ✓      | 20096.9    | 49.24        | 3.58          |
| trpc-router              | 9.27.3  | ✓      | 18866.9    | 52.47        | 4.17          |
| microrouter              | 3.1.3   | ✓      | 18801.5    | 52.67        | 3.35          |
| egg.js                   | 3.9.2   | ✓      | 10274.4    | 96.79        | 3.67          |
| express                  | 4.18.2  | ✓      | 8332.5     | 119.39       | 1.49          |
| fastify-big-json         | 4.11.0  | ✓      | 7177.6     | 138.65       | 82.58         |
| express-route-prefix     | 4.18.2  | ✓      | 7108.2     | 140.04       | 2.63          |
| express-with-middlewares | 4.18.2  | ✓      | 7050.1     | 141.16       | 2.62          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

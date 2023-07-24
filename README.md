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
* __Run:__ Mon Jul 24 2023 02:30:42 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 54594.4    | 17.83        | 9.74          |
| polkadot                 | 1.0.0   | ✗      | 54216.0    | 17.95        | 9.67          |
| 0http                    | 3.5.2   | ✓      | 52683.2    | 18.49        | 9.39          |
| foxify                   | 0.10.20 | ✓      | 52599.2    | 18.52        | 8.63          |
| micro                    | 9.4.1   | ✗      | 52209.6    | 18.66        | 9.31          |
| polka                    | 0.5.2   | ✓      | 52140.0    | 18.68        | 9.30          |
| h3                       | 0.8.6   | ✗      | 51889.6    | 18.78        | 8.51          |
| fastify                  | 4.20.0  | ✓      | 51846.4    | 18.80        | 9.30          |
| connect                  | 3.7.0   | ✗      | 50483.4    | 19.33        | 9.00          |
| server-base              | 7.1.32  | ✗      | 50069.6    | 19.47        | 8.93          |
| h3-router                | 0.8.6   | ✓      | 49546.4    | 19.69        | 8.13          |
| server-base-router       | 7.1.32  | ✓      | 48554.4    | 20.10        | 8.66          |
| restana                  | 4.9.7   | ✓      | 48191.2    | 20.25        | 8.59          |
| yeps                     | 1.1.1   | ✗      | 47784.8    | 20.43        | 8.52          |
| connect-router           | 1.3.8   | ✓      | 46731.2    | 20.91        | 8.33          |
| micro-route              | 2.5.0   | ✓      | 45127.2    | 21.66        | 8.05          |
| trek-engine              | 1.0.5   | ✗      | 44368.2    | 22.05        | 7.28          |
| trek-router              | 1.2.0   | ✓      | 42741.4    | 22.89        | 7.01          |
| vapr                     | 0.6.0   | ✓      | 41405.6    | 23.65        | 6.79          |
| yeps-router              | 1.2.0   | ✓      | 39149.8    | 25.04        | 6.98          |
| koa                      | 2.14.2  | ✗      | 39129.0    | 25.07        | 6.98          |
| spirit                   | 0.6.1   | ✗      | 37117.4    | 26.46        | 6.62          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36339.8    | 27.02        | 6.48          |
| total.js                 | 3.4.13  | ✓      | 36038.6    | 27.25        | 11.03         |
| spirit-router            | 0.5.0   | ✓      | 35780.6    | 27.46        | 6.38          |
| take-five                | 2.0.0   | ✓      | 35471.8    | 27.69        | 12.75         |
| restify                  | 8.6.1   | ✓      | 34795.8    | 28.24        | 6.27          |
| koa-router               | 12.0.0  | ✓      | 32282.2    | 30.47        | 5.76          |
| hapi                     | 20.3.0  | ✓      | 29139.6    | 33.82        | 5.20          |
| microrouter              | 3.1.3   | ✓      | 27799.6    | 35.46        | 4.96          |
| trpc-router              | 9.27.3  | ✓      | 23753.2    | 41.60        | 5.26          |
| egg.js                   | 3.17.3  | ✓      | 14504.6    | 68.43        | 5.19          |
| express                  | 4.18.2  | ✓      | 11887.2    | 83.58        | 2.12          |
| express-with-middlewares | 4.18.2  | ✓      | 10448.8    | 95.13        | 3.89          |
| fastify-big-json         | 4.20.0  | ✓      | 9848.5     | 101.03       | 113.31        |
| express-route-prefix     | 4.18.2  | ✓      | 8630.4     | 115.30       | 3.19          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

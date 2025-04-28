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
* __Run:__ Mon Apr 28 2025 02:54:39 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 64798.0    | 14.94        | 11.56         |
| polkadot                 | 1.0.0   | ✗      | 63810.8    | 15.18        | 11.38         |
| h3                       | 0.8.6   | ✗      | 60804.0    | 15.95        | 9.97          |
| h3-router                | 0.8.6   | ✓      | 60353.6    | 16.08        | 9.90          |
| bare                     | 10.13.0 | ✗      | 59492.8    | 16.31        | 10.61         |
| foxify                   | 0.10.20 | ✓      | 57325.6    | 16.94        | 9.40          |
| restana                  | 4.9.9   | ✓      | 56952.8    | 17.05        | 10.16         |
| polka                    | 0.5.2   | ✓      | 56480.8    | 17.21        | 10.07         |
| micro                    | 9.4.1   | ✗      | 55892.0    | 17.40        | 9.97          |
| connect                  | 3.7.0   | ✗      | 55153.6    | 17.63        | 9.84          |
| fastify                  | 4.29.0  | ✓      | 54120.8    | 17.98        | 9.70          |
| server-base-router       | 7.1.32  | ✓      | 53464.0    | 18.20        | 9.53          |
| server-base              | 7.1.32  | ✗      | 51737.6    | 18.83        | 9.23          |
| yeps                     | 1.1.1   | ✗      | 50576.8    | 19.27        | 9.02          |
| micro-route              | 2.5.0   | ✓      | 48292.8    | 20.22        | 8.61          |
| trek-engine              | 1.0.5   | ✗      | 48268.8    | 20.22        | 7.92          |
| connect-router           | 1.3.8   | ✓      | 48024.8    | 20.32        | 8.56          |
| trek-router              | 1.2.0   | ✓      | 46048.8    | 21.22        | 7.55          |
| vapr                     | 0.6.0   | ✓      | 44601.6    | 21.92        | 7.32          |
| yeps-router              | 1.2.0   | ✓      | 41969.6    | 23.33        | 7.48          |
| spirit                   | 0.6.1   | ✗      | 41700.0    | 23.49        | 7.44          |
| koa                      | 2.16.1  | ✗      | 41650.2    | 23.51        | 7.43          |
| spirit-router            | 0.5.0   | ✓      | 40491.2    | 24.20        | 7.22          |
| total.js                 | 3.4.13  | ✓      | 39321.6    | 24.92        | 12.04         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38672.6    | 25.36        | 6.90          |
| restify                  | 8.6.1   | ✓      | 38376.2    | 25.55        | 6.92          |
| take-five                | 2.0.0   | ✓      | 37501.8    | 26.17        | 13.48         |
| koa-router               | 12.0.1  | ✓      | 35029.0    | 28.05        | 6.25          |
| hapi                     | 20.3.0  | ✓      | 32504.6    | 30.26        | 5.80          |
| microrouter              | 3.1.3   | ✓      | 31184.0    | 31.56        | 5.56          |
| trpc-router              | 9.27.4  | ✓      | 26910.8    | 36.65        | 5.95          |
| egg.js                   | 3.30.1  | ✓      | 16168.1    | 61.32        | 5.78          |
| express                  | 4.21.2  | ✓      | 13109.2    | 75.71        | 2.34          |
| fastify-big-json         | 4.29.0  | ✓      | 12521.2    | 79.32        | 144.06        |
| express-with-middlewares | 4.21.2  | ✓      | 12154.6    | 81.72        | 4.52          |
| express-route-prefix     | 4.21.2  | ✓      | 10771.4    | 92.26        | 3.99          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

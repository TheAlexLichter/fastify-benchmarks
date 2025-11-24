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
* __Run:__ Mon Nov 24 2025 03:07:59 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69088.4    | 13.97        | 12.32         |
| 0http                    | 3.5.3   | ✓      | 65425.2    | 14.79        | 11.67         |
| restana                  | 4.9.9   | ✓      | 62016.8    | 15.61        | 11.06         |
| h3                       | 0.8.6   | ✗      | 61171.2    | 15.86        | 10.03         |
| bare                     | 10.13.0 | ✗      | 60202.4    | 16.10        | 10.74         |
| h3-router                | 0.8.6   | ✓      | 59471.2    | 16.32        | 9.75          |
| polka                    | 0.5.2   | ✓      | 58454.4    | 16.61        | 10.42         |
| foxify                   | 0.10.20 | ✓      | 58102.4    | 16.71        | 9.53          |
| connect                  | 3.7.0   | ✗      | 57088.8    | 17.02        | 10.18         |
| micro                    | 9.4.1   | ✗      | 55338.4    | 17.57        | 9.87          |
| fastify                  | 4.29.1  | ✓      | 55153.6    | 17.63        | 9.89          |
| server-base              | 7.1.32  | ✗      | 54898.4    | 17.72        | 9.79          |
| server-base-router       | 7.1.32  | ✓      | 54016.0    | 18.02        | 9.63          |
| yeps                     | 1.1.1   | ✗      | 50608.8    | 19.26        | 9.03          |
| micro-route              | 2.5.0   | ✓      | 49463.2    | 19.72        | 8.82          |
| connect-router           | 1.3.8   | ✓      | 48087.2    | 20.30        | 8.58          |
| trek-engine              | 1.0.5   | ✗      | 47017.6    | 20.77        | 7.71          |
| trek-router              | 1.2.0   | ✓      | 45339.2    | 21.56        | 7.44          |
| vapr                     | 0.6.0   | ✓      | 43839.2    | 22.31        | 7.19          |
| yeps-router              | 1.2.0   | ✓      | 42136.0    | 23.23        | 7.51          |
| spirit                   | 0.6.1   | ✗      | 40859.2    | 23.98        | 7.29          |
| koa                      | 2.16.3  | ✗      | 40442.4    | 24.23        | 7.21          |
| spirit-router            | 0.5.0   | ✓      | 40399.2    | 24.26        | 7.21          |
| total.js                 | 3.4.13  | ✓      | 38966.4    | 25.16        | 11.93         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38437.4    | 25.52        | 6.85          |
| take-five                | 2.0.0   | ✓      | 37999.8    | 25.82        | 13.66         |
| restify                  | 8.6.1   | ✓      | 37183.4    | 26.40        | 6.70          |
| koa-router               | 12.0.1  | ✓      | 34967.0    | 28.10        | 6.24          |
| hapi                     | 20.3.0  | ✓      | 33026.6    | 29.78        | 5.89          |
| microrouter              | 3.1.3   | ✓      | 31752.8    | 31.00        | 5.66          |
| trpc-router              | 9.27.4  | ✓      | 25854.8    | 38.16        | 5.72          |
| egg.js                   | 3.31.0  | ✓      | 17425.4    | 56.88        | 6.23          |
| express                  | 4.21.2  | ✓      | 12994.0    | 76.39        | 2.32          |
| fastify-big-json         | 4.29.1  | ✓      | 12576.8    | 78.98        | 144.70        |
| express-with-middlewares | 4.21.2  | ✓      | 12181.0    | 81.55        | 4.53          |
| express-route-prefix     | 4.21.2  | ✓      | 10445.4    | 95.15        | 3.87          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jun 09 2025 03:09:41 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 70422.8    | 13.70        | 12.56         |
| 0http                    | 3.5.3   | ✓      | 68181.2    | 14.17        | 12.16         |
| h3-router                | 0.8.6   | ✓      | 64627.2    | 14.98        | 10.60         |
| restana                  | 4.9.9   | ✓      | 62523.2    | 15.48        | 11.15         |
| h3                       | 0.8.6   | ✗      | 61303.6    | 15.83        | 10.06         |
| bare                     | 10.13.0 | ✗      | 60904.8    | 15.93        | 10.86         |
| polka                    | 0.5.2   | ✓      | 59367.2    | 16.34        | 10.59         |
| foxify                   | 0.10.20 | ✓      | 58488.8    | 16.60        | 9.59          |
| connect                  | 3.7.0   | ✗      | 57852.0    | 16.79        | 10.32         |
| fastify                  | 4.29.1  | ✓      | 56528.8    | 17.20        | 10.13         |
| micro                    | 9.4.1   | ✗      | 56168.0    | 17.30        | 10.02         |
| server-base-router       | 7.1.32  | ✓      | 54594.4    | 17.82        | 9.74          |
| server-base              | 7.1.32  | ✗      | 54369.6    | 17.91        | 9.70          |
| yeps                     | 1.1.1   | ✗      | 52131.2    | 18.69        | 9.30          |
| connect-router           | 1.3.8   | ✓      | 51896.0    | 18.78        | 9.25          |
| micro-route              | 2.5.0   | ✓      | 50135.2    | 19.45        | 8.94          |
| trek-engine              | 1.0.5   | ✗      | 47528.0    | 20.54        | 7.80          |
| vapr                     | 0.6.0   | ✓      | 46431.2    | 21.04        | 7.62          |
| trek-router              | 1.2.0   | ✓      | 45483.2    | 21.49        | 7.46          |
| yeps-router              | 1.2.0   | ✓      | 42758.4    | 22.88        | 7.63          |
| koa                      | 2.16.1  | ✗      | 42025.6    | 23.30        | 7.49          |
| spirit-router            | 0.5.0   | ✓      | 40648.8    | 24.10        | 7.25          |
| spirit                   | 0.6.1   | ✗      | 40116.8    | 24.43        | 7.15          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39662.2    | 24.71        | 7.07          |
| take-five                | 2.0.0   | ✓      | 39413.4    | 24.87        | 14.17         |
| restify                  | 8.6.1   | ✓      | 38890.2    | 25.22        | 7.01          |
| total.js                 | 3.4.13  | ✓      | 38670.6    | 25.36        | 11.84         |
| koa-router               | 12.0.1  | ✓      | 35796.2    | 27.43        | 6.38          |
| hapi                     | 20.3.0  | ✓      | 32415.0    | 30.35        | 5.78          |
| microrouter              | 3.1.3   | ✓      | 32180.0    | 30.57        | 5.74          |
| trpc-router              | 9.27.4  | ✓      | 26947.2    | 36.60        | 5.96          |
| egg.js                   | 3.30.1  | ✓      | 17840.7    | 55.52        | 6.38          |
| express                  | 4.21.2  | ✓      | 13310.4    | 74.56        | 2.37          |
| fastify-big-json         | 4.29.1  | ✓      | 12719.4    | 78.05        | 146.35        |
| express-with-middlewares | 4.21.2  | ✓      | 12204.6    | 81.38        | 4.54          |
| express-route-prefix     | 4.21.2  | ✓      | 10719.9    | 92.69        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

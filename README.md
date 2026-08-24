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
* __Run:__ Mon Aug 24 2026 02:38:46 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 117366.4   | 8.03         | 20.93         |
| foxify                   | 0.10.20 | ✓      | 115636.8   | 8.15         | 18.97         |
| 0http                    | 3.5.3   | ✓      | 113558.4   | 8.31         | 20.25         |
| connect                  | 3.7.0   | ✗      | 112001.6   | 8.44         | 19.97         |
| polka                    | 0.5.2   | ✓      | 108790.4   | 8.70         | 19.40         |
| micro                    | 9.4.1   | ✗      | 108502.4   | 8.72         | 19.35         |
| fastify                  | 4.29.1  | ✓      | 108468.8   | 8.72         | 19.45         |
| polkadot                 | 1.0.0   | ✗      | 108280.0   | 8.74         | 19.31         |
| h3                       | 0.8.6   | ✗      | 106798.4   | 8.86         | 17.52         |
| h3-router                | 0.8.6   | ✓      | 106496.0   | 8.90         | 17.47         |
| connect-router           | 1.3.8   | ✓      | 104998.4   | 9.03         | 18.73         |
| yeps                     | 1.1.1   | ✗      | 103750.4   | 9.14         | 18.50         |
| restana                  | 4.9.9   | ✓      | 102395.2   | 9.27         | 18.26         |
| micro-route              | 2.5.0   | ✓      | 99811.2    | 9.53         | 17.80         |
| server-base              | 7.1.32  | ✗      | 98841.6    | 9.62         | 17.63         |
| server-base-router       | 7.1.32  | ✓      | 97851.2    | 9.72         | 17.45         |
| trek-engine              | 1.0.5   | ✗      | 93398.4    | 10.21        | 15.32         |
| vapr                     | 0.6.0   | ✓      | 89094.4    | 10.72        | 14.61         |
| trek-router              | 1.2.0   | ✓      | 88803.2    | 10.77        | 14.57         |
| total.js                 | 3.4.13  | ✓      | 78333.2    | 12.27        | 23.98         |
| yeps-router              | 1.2.0   | ✓      | 76648.4    | 12.55        | 13.67         |
| take-five                | 2.0.0   | ✓      | 74513.2    | 12.92        | 26.79         |
| koa                      | 2.16.4  | ✗      | 71196.0    | 13.55        | 12.70         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 67541.6    | 14.31        | 12.04         |
| spirit                   | 0.6.1   | ✗      | 67234.0    | 14.37        | 11.99         |
| koa-router               | 12.0.1  | ✓      | 65412.0    | 14.79        | 11.66         |
| restify                  | 8.6.1   | ✓      | 65214.8    | 14.84        | 11.75         |
| spirit-router            | 0.5.0   | ✓      | 65135.6    | 14.86        | 11.62         |
| hapi                     | 20.3.0  | ✓      | 60360.8    | 16.07        | 10.76         |
| microrouter              | 3.1.3   | ✓      | 58984.8    | 16.45        | 10.52         |
| trpc-router              | 9.27.4  | ✓      | 49385.6    | 19.75        | 10.93         |
| egg.js                   | 3.34.0  | ✓      | 24600.0    | 40.14        | 8.80          |
| express                  | 4.22.2  | ✓      | 23081.6    | 42.81        | 4.12          |
| express-with-middlewares | 4.22.2  | ✓      | 20182.4    | 49.01        | 7.51          |
| fastify-big-json         | 4.29.1  | ✓      | 16940.2    | 58.52        | 194.91        |
| express-route-prefix     | 4.22.2  | ✓      | 15875.5    | 62.45        | 5.87          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

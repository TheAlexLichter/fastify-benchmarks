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
* __Run:__ Mon Jul 28 2025 03:20:19 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68501.2    | 14.10        | 12.22         |
| polkadot                 | 1.0.0   | ✗      | 66452.0    | 14.55        | 11.85         |
| h3-router                | 0.8.6   | ✓      | 65775.2    | 14.70        | 10.79         |
| h3                       | 0.8.6   | ✗      | 64252.0    | 15.07        | 10.54         |
| bare                     | 10.13.0 | ✗      | 61768.0    | 15.69        | 11.02         |
| foxify                   | 0.10.20 | ✓      | 59706.4    | 16.25        | 9.79          |
| restana                  | 4.9.9   | ✓      | 59562.4    | 16.29        | 10.62         |
| polka                    | 0.5.2   | ✓      | 58265.6    | 16.67        | 10.39         |
| connect                  | 3.7.0   | ✗      | 57016.0    | 17.03        | 10.17         |
| fastify                  | 4.29.1  | ✓      | 56944.8    | 17.06        | 10.21         |
| micro                    | 9.4.1   | ✗      | 55513.6    | 17.52        | 9.90          |
| server-base-router       | 7.1.32  | ✓      | 55070.4    | 17.65        | 9.82          |
| server-base              | 7.1.32  | ✗      | 53009.6    | 18.37        | 9.45          |
| yeps                     | 1.1.1   | ✗      | 51626.4    | 18.86        | 9.21          |
| micro-route              | 2.5.0   | ✓      | 50550.4    | 19.28        | 9.01          |
| trek-engine              | 1.0.5   | ✗      | 49923.2    | 19.53        | 8.19          |
| connect-router           | 1.3.8   | ✓      | 49680.8    | 19.63        | 8.86          |
| trek-router              | 1.2.0   | ✓      | 48131.2    | 20.28        | 7.89          |
| vapr                     | 0.6.0   | ✓      | 47811.2    | 20.42        | 7.84          |
| yeps-router              | 1.2.0   | ✓      | 45389.6    | 21.55        | 8.09          |
| spirit                   | 0.6.1   | ✗      | 45064.8    | 21.72        | 8.04          |
| koa                      | 2.16.1  | ✗      | 43453.6    | 22.51        | 7.75          |
| spirit-router            | 0.5.0   | ✓      | 42999.2    | 22.75        | 7.67          |
| total.js                 | 3.4.13  | ✓      | 40432.8    | 24.24        | 12.38         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39546.6    | 24.78        | 7.05          |
| restify                  | 8.6.1   | ✓      | 39454.6    | 24.85        | 7.11          |
| take-five                | 2.0.0   | ✓      | 39237.8    | 24.98        | 14.11         |
| koa-router               | 12.0.1  | ✓      | 36827.8    | 26.65        | 6.57          |
| hapi                     | 20.3.0  | ✓      | 34140.6    | 28.79        | 6.09          |
| microrouter              | 3.1.3   | ✓      | 31683.4    | 31.06        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 28166.0    | 35.00        | 6.23          |
| egg.js                   | 3.31.0  | ✓      | 17784.7    | 55.71        | 6.36          |
| express                  | 4.21.2  | ✓      | 13756.0    | 72.16        | 2.45          |
| fastify-big-json         | 4.29.1  | ✓      | 12881.8    | 77.09        | 148.22        |
| express-with-middlewares | 4.21.2  | ✓      | 12509.8    | 79.38        | 4.65          |
| express-route-prefix     | 4.21.2  | ✓      | 11125.6    | 89.31        | 4.12          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

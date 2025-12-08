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
* __Run:__ Mon Dec 08 2025 02:59:46 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67604.0    | 14.31        | 12.06         |
| 0http                    | 3.5.3   | ✓      | 65996.4    | 14.66        | 11.77         |
| h3-router                | 0.8.6   | ✓      | 63744.0    | 15.19        | 10.46         |
| restana                  | 4.9.9   | ✓      | 62337.6    | 15.54        | 11.12         |
| h3                       | 0.8.6   | ✗      | 62129.6    | 15.60        | 10.19         |
| bare                     | 10.13.0 | ✗      | 60016.8    | 16.17        | 10.70         |
| foxify                   | 0.10.20 | ✓      | 59676.0    | 16.26        | 9.79          |
| polka                    | 0.5.2   | ✓      | 57876.0    | 16.78        | 10.32         |
| connect                  | 3.7.0   | ✗      | 57213.6    | 16.98        | 10.20         |
| fastify                  | 4.29.1  | ✓      | 57213.6    | 16.98        | 10.26         |
| micro                    | 9.4.1   | ✗      | 56251.2    | 17.28        | 10.03         |
| server-base              | 7.1.32  | ✗      | 55301.6    | 17.58        | 9.86          |
| server-base-router       | 7.1.32  | ✓      | 54758.4    | 17.76        | 9.77          |
| yeps                     | 1.1.1   | ✗      | 51476.8    | 18.93        | 9.18          |
| connect-router           | 1.3.8   | ✓      | 50664.0    | 19.24        | 9.03          |
| micro-route              | 2.5.0   | ✓      | 50653.6    | 19.24        | 9.03          |
| trek-engine              | 1.0.5   | ✗      | 47476.0    | 20.57        | 7.79          |
| trek-router              | 1.2.0   | ✓      | 46724.8    | 20.91        | 7.66          |
| vapr                     | 0.6.0   | ✓      | 45439.2    | 21.50        | 7.45          |
| yeps-router              | 1.2.0   | ✓      | 43270.4    | 22.61        | 7.72          |
| spirit                   | 0.6.1   | ✗      | 42652.0    | 22.94        | 7.61          |
| koa                      | 2.16.3  | ✗      | 41232.0    | 23.76        | 7.35          |
| total.js                 | 3.4.13  | ✓      | 39160.8    | 25.04        | 11.99         |
| spirit-router            | 0.5.0   | ✓      | 38782.4    | 25.28        | 6.92          |
| restify                  | 8.6.1   | ✓      | 38711.2    | 25.33        | 6.98          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38443.0    | 25.51        | 6.86          |
| take-five                | 2.0.0   | ✓      | 37857.8    | 25.92        | 13.61         |
| koa-router               | 12.0.1  | ✓      | 36081.4    | 27.22        | 6.43          |
| hapi                     | 20.3.0  | ✓      | 32652.2    | 30.13        | 5.82          |
| microrouter              | 3.1.3   | ✓      | 31286.0    | 31.46        | 5.58          |
| trpc-router              | 9.27.4  | ✓      | 26876.0    | 36.71        | 5.95          |
| egg.js                   | 3.31.0  | ✓      | 16885.3    | 58.69        | 6.04          |
| express                  | 4.22.1  | ✓      | 13667.4    | 72.63        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12770.0    | 77.76        | 146.92        |
| express-with-middlewares | 4.22.1  | ✓      | 12196.4    | 81.43        | 4.54          |
| express-route-prefix     | 4.22.1  | ✓      | 10874.0    | 91.38        | 4.02          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

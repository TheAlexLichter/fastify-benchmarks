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
* __Run:__ Mon Jun 24 2024 02:23:55 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68400.8    | 14.13        | 12.20         |
| 0http                    | 3.5.3   | ✓      | 67897.2    | 14.23        | 12.11         |
| h3                       | 0.8.6   | ✗      | 64660.8    | 14.97        | 10.61         |
| h3-router                | 0.8.6   | ✓      | 63674.4    | 15.22        | 10.44         |
| bare                     | 10.13.0 | ✗      | 60700.8    | 15.97        | 10.82         |
| foxify                   | 0.10.20 | ✓      | 60019.2    | 16.16        | 9.84          |
| restana                  | 4.9.9   | ✓      | 60013.6    | 16.19        | 10.70         |
| connect                  | 3.7.0   | ✗      | 58940.8    | 16.47        | 10.51         |
| polka                    | 0.5.2   | ✓      | 58519.2    | 16.59        | 10.44         |
| fastify                  | 4.28.0  | ✓      | 56134.4    | 17.32        | 10.06         |
| micro                    | 9.4.1   | ✗      | 55652.8    | 17.47        | 9.92          |
| server-base-router       | 7.1.32  | ✓      | 55135.2    | 17.64        | 9.83          |
| server-base              | 7.1.32  | ✗      | 55117.6    | 17.64        | 9.83          |
| yeps                     | 1.1.1   | ✗      | 52415.2    | 18.58        | 9.35          |
| connect-router           | 1.3.8   | ✓      | 51031.2    | 19.10        | 9.10          |
| micro-route              | 2.5.0   | ✓      | 50495.2    | 19.31        | 9.01          |
| trek-engine              | 1.0.5   | ✗      | 49361.6    | 19.76        | 8.10          |
| trek-router              | 1.2.0   | ✓      | 48916.8    | 19.95        | 8.02          |
| vapr                     | 0.6.0   | ✓      | 47369.6    | 20.62        | 7.77          |
| spirit                   | 0.6.1   | ✗      | 45415.2    | 21.56        | 8.10          |
| yeps-router              | 1.2.0   | ✓      | 43840.0    | 22.31        | 7.82          |
| koa                      | 2.15.3  | ✗      | 42978.4    | 22.77        | 7.66          |
| spirit-router            | 0.5.0   | ✓      | 41660.8    | 23.47        | 7.43          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40221.8    | 24.37        | 7.17          |
| total.js                 | 3.4.13  | ✓      | 39677.0    | 24.70        | 12.15         |
| restify                  | 8.6.1   | ✓      | 39544.6    | 24.79        | 7.13          |
| take-five                | 2.0.0   | ✓      | 38731.4    | 25.32        | 13.93         |
| koa-router               | 12.0.1  | ✓      | 37572.6    | 26.12        | 6.70          |
| hapi                     | 20.3.0  | ✓      | 34437.8    | 28.54        | 6.14          |
| microrouter              | 3.1.3   | ✓      | 32141.6    | 30.60        | 5.73          |
| trpc-router              | 9.27.4  | ✓      | 26728.4    | 36.91        | 5.91          |
| egg.js                   | 3.24.1  | ✓      | 17788.7    | 55.69        | 6.36          |
| express                  | 4.19.2  | ✓      | 13412.0    | 74.00        | 2.39          |
| fastify-big-json         | 4.28.0  | ✓      | 13027.4    | 76.21        | 149.89        |
| express-with-middlewares | 4.19.2  | ✓      | 12705.0    | 78.16        | 4.73          |
| express-route-prefix     | 4.19.2  | ✓      | 11040.4    | 90.00        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

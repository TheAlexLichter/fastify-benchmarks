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
* __Node:__ `v14.21.2`
* __Run:__ Mon Feb 20 2023 02:40:14 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 62196.0    | 15.59        | 11.09         |
| polkadot                 | 1.0.0   | ✗      | 62179.2    | 15.58        | 11.09         |
| foxify                   | 0.10.20 | ✓      | 61340.8    | 15.80        | 10.06         |
| 0http                    | 3.4.4   | ✓      | 61060.8    | 15.90        | 10.89         |
| h3                       | 0.8.6   | ✗      | 60593.6    | 15.99        | 9.94          |
| h3-router                | 0.8.6   | ✓      | 60580.0    | 16.01        | 9.94          |
| fastify                  | 4.13.0  | ✓      | 59157.6    | 16.41        | 10.61         |
| polka                    | 0.5.2   | ✓      | 58899.2    | 16.48        | 10.50         |
| micro                    | 9.4.1   | ✗      | 58536.0    | 16.59        | 10.44         |
| connect                  | 3.7.0   | ✗      | 57159.2    | 17.01        | 10.19         |
| server-base-router       | 7.1.32  | ✓      | 56450.4    | 17.21        | 10.07         |
| restana                  | 4.9.7   | ✓      | 55434.4    | 17.50        | 9.89          |
| yeps                     | 1.1.1   | ✗      | 55194.4    | 17.62        | 9.84          |
| server-base              | 7.1.32  | ✗      | 55061.6    | 17.66        | 9.82          |
| connect-router           | 1.3.7   | ✓      | 53532.0    | 18.19        | 9.55          |
| micro-route              | 2.5.0   | ✓      | 53053.6    | 18.36        | 9.46          |
| trek-router              | 1.2.0   | ✓      | 50148.0    | 19.44        | 8.23          |
| trek-engine              | 1.0.5   | ✗      | 49825.6    | 19.58        | 8.17          |
| vapr                     | 0.6.0   | ✓      | 49265.6    | 19.81        | 8.08          |
| yeps-router              | 1.2.0   | ✓      | 45732.0    | 21.37        | 8.16          |
| spirit                   | 0.6.1   | ✗      | 44823.2    | 21.82        | 7.99          |
| koa                      | 2.14.1  | ✗      | 44197.6    | 22.13        | 7.88          |
| spirit-router            | 0.5.0   | ✓      | 43558.4    | 22.47        | 7.77          |
| take-five                | 2.0.0   | ✓      | 42370.4    | 23.12        | 15.23         |
| total.js                 | 3.4.13  | ✓      | 40920.8    | 23.92        | 12.53         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40506.2    | 24.19        | 7.22          |
| restify                  | 8.6.1   | ✓      | 39629.4    | 24.73        | 7.14          |
| koa-router               | 12.0.0  | ✓      | 38359.2    | 25.58        | 6.84          |
| hapi                     | 20.3.0  | ✓      | 34359.2    | 28.61        | 6.13          |
| microrouter              | 3.1.3   | ✓      | 32402.2    | 30.36        | 5.78          |
| trpc-router              | 9.27.3  | ✓      | 28157.6    | 35.01        | 6.23          |
| egg.js                   | 3.15.0  | ✓      | 16602.1    | 59.76        | 5.94          |
| express                  | 4.18.2  | ✓      | 13869.6    | 71.59        | 2.47          |
| express-with-middlewares | 4.18.2  | ✓      | 12124.8    | 81.94        | 4.51          |
| express-route-prefix     | 4.18.2  | ✓      | 12001.2    | 82.79        | 4.44          |
| fastify-big-json         | 4.13.0  | ✓      | 11421.4    | 87.08        | 131.41        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

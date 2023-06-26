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
* __Run:__ Mon Jun 26 2023 02:52:52 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 32394.4    | 30.42        | 5.78          |
| micro                    | 9.4.1   | ✗      | 31677.6    | 31.08        | 5.65          |
| 0http                    | 3.5.2   | ✓      | 30743.4    | 32.06        | 5.48          |
| foxify                   | 0.10.20 | ✓      | 30113.6    | 32.75        | 4.94          |
| h3-router                | 0.8.6   | ✓      | 28545.6    | 34.57        | 4.68          |
| bare                     | 10.13.0 | ✗      | 27944.0    | 35.32        | 4.98          |
| server-base              | 7.1.32  | ✗      | 27920.0    | 35.34        | 4.98          |
| h3                       | 0.8.6   | ✗      | 27898.4    | 35.37        | 4.58          |
| polka                    | 0.5.2   | ✓      | 27484.8    | 35.90        | 4.90          |
| server-base-router       | 7.1.32  | ✓      | 27480.4    | 35.91        | 4.90          |
| connect                  | 3.7.0   | ✗      | 26944.0    | 36.65        | 4.80          |
| fastify                  | 4.18.0  | ✓      | 26556.0    | 37.16        | 4.76          |
| yeps                     | 1.1.1   | ✗      | 25967.6    | 38.03        | 4.63          |
| spirit-router            | 0.5.0   | ✓      | 25889.2    | 38.24        | 4.62          |
| micro-route              | 2.5.0   | ✓      | 25850.8    | 38.18        | 4.61          |
| trek-engine              | 1.0.5   | ✗      | 25084.4    | 39.40        | 4.11          |
| spirit                   | 0.6.1   | ✗      | 24736.4    | 39.99        | 4.41          |
| connect-router           | 1.3.8   | ✓      | 23532.4    | 41.99        | 4.20          |
| trek-router              | 1.2.0   | ✓      | 23356.1    | 42.31        | 3.83          |
| restana                  | 4.9.7   | ✓      | 22978.0    | 43.01        | 4.10          |
| yeps-router              | 1.2.0   | ✓      | 22626.8    | 43.69        | 4.03          |
| koa                      | 2.14.2  | ✗      | 21180.0    | 46.73        | 3.78          |
| vapr                     | 0.6.0   | ✓      | 21036.7    | 47.04        | 3.45          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20831.7    | 47.49        | 3.72          |
| total.js                 | 3.4.13  | ✓      | 20358.9    | 48.61        | 6.23          |
| take-five                | 2.0.0   | ✓      | 19155.1    | 51.69        | 6.89          |
| restify                  | 8.6.1   | ✓      | 19023.9    | 52.05        | 3.43          |
| koa-router               | 12.0.0  | ✓      | 18803.9    | 52.66        | 3.35          |
| hapi                     | 20.3.0  | ✓      | 18555.6    | 53.37        | 3.31          |
| microrouter              | 3.1.3   | ✓      | 17162.2    | 57.75        | 3.06          |
| trpc-router              | 9.27.3  | ✓      | 16780.0    | 59.07        | 3.71          |
| egg.js                   | 3.17.2  | ✓      | 8359.3     | 119.06       | 2.99          |
| express                  | 4.18.2  | ✓      | 7549.9     | 131.74       | 1.35          |
| fastify-big-json         | 4.18.0  | ✓      | 6793.3     | 146.58       | 78.16         |
| express-route-prefix     | 4.18.2  | ✓      | 6756.9     | 147.27       | 2.50          |
| express-with-middlewares | 4.18.2  | ✓      | 6238.6     | 159.65       | 2.32          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

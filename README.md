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
* __Run:__ Mon May 01 2023 02:29:00 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| micro                    | 9.4.1   | ✗      | 32208.4    | 30.55        | 5.74          |
| polkadot                 | 1.0.0   | ✗      | 31689.8    | 31.07        | 5.65          |
| h3-router                | 0.8.6   | ✓      | 30992.0    | 31.77        | 5.08          |
| foxify                   | 0.10.20 | ✓      | 30838.0    | 31.93        | 5.06          |
| bare                     | 10.13.0 | ✗      | 30004.4    | 32.87        | 5.35          |
| fastify                  | 4.17.0  | ✓      | 29890.4    | 32.95        | 5.36          |
| polka                    | 0.5.2   | ✓      | 29860.8    | 33.00        | 5.33          |
| 0http                    | 3.5.2   | ✓      | 29167.2    | 33.80        | 5.20          |
| h3                       | 0.8.6   | ✗      | 28645.6    | 34.44        | 4.70          |
| server-base              | 7.1.32  | ✗      | 27735.2    | 35.55        | 4.95          |
| connect                  | 3.7.0   | ✗      | 26995.6    | 36.57        | 4.81          |
| restana                  | 4.9.7   | ✓      | 26876.0    | 36.72        | 4.79          |
| server-base-router       | 7.1.32  | ✓      | 26844.0    | 36.75        | 4.79          |
| connect-router           | 1.3.8   | ✓      | 26070.8    | 37.87        | 4.65          |
| yeps                     | 1.1.1   | ✗      | 26004.4    | 37.95        | 4.64          |
| micro-route              | 2.5.0   | ✓      | 25860.4    | 38.16        | 4.61          |
| trek-engine              | 1.0.5   | ✗      | 25547.3    | 38.64        | 4.19          |
| spirit                   | 0.6.1   | ✗      | 23913.6    | 41.36        | 4.26          |
| trek-router              | 1.2.0   | ✓      | 23740.1    | 41.62        | 3.89          |
| yeps-router              | 1.2.0   | ✓      | 23182.4    | 42.63        | 4.13          |
| vapr                     | 0.6.0   | ✓      | 23149.6    | 42.69        | 3.80          |
| koa                      | 2.14.2  | ✗      | 22805.2    | 43.36        | 4.07          |
| spirit-router            | 0.5.0   | ✓      | 22508.4    | 44.00        | 4.01          |
| restify                  | 8.6.1   | ✓      | 20799.1    | 47.58        | 3.75          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20156.9    | 49.11        | 3.59          |
| take-five                | 2.0.0   | ✓      | 20076.5    | 49.32        | 7.22          |
| total.js                 | 3.4.13  | ✓      | 19206.1    | 51.56        | 5.88          |
| koa-router               | 12.0.0  | ✓      | 19096.9    | 51.86        | 3.41          |
| hapi                     | 20.3.0  | ✓      | 18995.9    | 52.11        | 3.39          |
| microrouter              | 3.1.3   | ✓      | 17642.4    | 56.17        | 3.15          |
| trpc-router              | 9.27.3  | ✓      | 17607.5    | 56.30        | 3.90          |
| egg.js                   | 3.15.0  | ✓      | 9381.1     | 106.02       | 3.35          |
| express                  | 4.18.2  | ✓      | 7402.4     | 134.47       | 1.32          |
| fastify-big-json         | 4.17.0  | ✓      | 6913.0     | 144.10       | 79.54         |
| express-route-prefix     | 4.18.2  | ✓      | 6768.3     | 147.05       | 2.50          |
| express-with-middlewares | 4.18.2  | ✓      | 6280.2     | 158.51       | 2.34          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

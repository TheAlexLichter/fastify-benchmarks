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
* __Node:__ `v14.20.1`
* __Run:__ Mon Nov 14 2022 02:57:05 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 32694.2    | 30.13        | 5.83          |
| foxify                   | 0.10.20 | ✓      | 30998.0    | 31.76        | 5.08          |
| micro                    | 9.4.1   | ✗      | 30918.8    | 31.86        | 5.51          |
| h3                       | 0.8.6   | ✗      | 30707.2    | 32.07        | 5.04          |
| bare                     | 10.13.0 | ✗      | 30319.6    | 32.49        | 5.41          |
| 0http                    | 3.4.1   | ✓      | 29884.0    | 32.96        | 5.33          |
| polka                    | 0.5.2   | ✓      | 29710.4    | 33.17        | 5.30          |
| h3-router                | 0.8.6   | ✓      | 28964.0    | 34.03        | 4.75          |
| fastify                  | 4.9.2   | ✓      | 28695.6    | 34.35        | 5.14          |
| server-base              | 7.1.32  | ✗      | 28484.0    | 34.60        | 5.08          |
| spirit-router            | 0.5.0   | ✓      | 27212.8    | 36.39        | 4.85          |
| connect                  | 3.7.0   | ✗      | 26968.3    | 36.62        | 4.81          |
| yeps                     | 1.1.1   | ✗      | 26780.0    | 36.85        | 4.78          |
| server-base-router       | 7.1.32  | ✓      | 26749.6    | 36.88        | 4.77          |
| rayo                     | 1.3.10  | ✓      | 26536.8    | 37.18        | 4.73          |
| spirit                   | 0.6.1   | ✗      | 26354.4    | 37.60        | 4.70          |
| connect-router           | 1.3.7   | ✓      | 25048.4    | 39.42        | 4.47          |
| micro-route              | 2.5.0   | ✓      | 24514.0    | 40.28        | 4.37          |
| trek-engine              | 1.0.5   | ✗      | 23691.2    | 41.75        | 3.89          |
| trek-router              | 1.2.0   | ✓      | 23683.1    | 41.75        | 3.88          |
| restana                  | 4.9.6   | ✓      | 23487.1    | 42.06        | 4.19          |
| yeps-router              | 1.2.0   | ✓      | 22650.8    | 43.63        | 4.04          |
| vapr                     | 0.6.0   | ✓      | 22240.0    | 44.45        | 3.65          |
| koa                      | 2.13.4  | ✗      | 21054.9    | 47.02        | 3.75          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 19711.3    | 50.22        | 3.51          |
| take-five                | 2.0.0   | ✓      | 19427.9    | 50.97        | 6.98          |
| total.js                 | 3.4.13  | ✓      | 19009.5    | 52.13        | 5.82          |
| hapi                     | 20.2.2  | ✓      | 18935.5    | 52.28        | 3.38          |
| koa-router               | 12.0.0  | ✓      | 18863.6    | 52.52        | 3.36          |
| restify                  | 8.6.1   | ✓      | 18750.5    | 52.82        | 3.38          |
| microrouter              | 3.1.3   | ✓      | 16345.9    | 60.66        | 2.92          |
| trpc-router              | 9.27.4  | ✓      | 15198.2    | 65.28        | 3.36          |
| egg.js                   | 3.3.3   | ✓      | 10012.0    | 99.29        | 3.58          |
| express                  | 4.18.2  | ✓      | 6822.0     | 145.89       | 1.22          |
| fastify-big-json         | 4.9.2   | ✓      | 6606.7     | 150.85       | 76.01         |
| express-route-prefix     | 4.18.2  | ✓      | 6334.9     | 157.21       | 2.34          |
| express-with-middlewares | 4.18.2  | ✓      | 5915.6     | 168.34       | 2.20          |

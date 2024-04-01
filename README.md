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
* __Run:__ Mon Apr 01 2024 02:13:56 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 65694.0    | 14.73        | 11.71         |
| 0http                    | 3.5.2   | ✓      | 62802.4    | 15.43        | 11.20         |
| h3                       | 0.8.6   | ✗      | 61518.4    | 15.75        | 10.09         |
| h3-router                | 0.8.6   | ✓      | 61089.6    | 15.87        | 10.02         |
| polka                    | 0.5.2   | ✓      | 58912.8    | 16.48        | 10.51         |
| foxify                   | 0.10.20 | ✓      | 58198.4    | 16.68        | 9.55          |
| bare                     | 10.13.0 | ✗      | 57949.6    | 16.76        | 10.33         |
| connect                  | 3.7.0   | ✗      | 56390.4    | 17.24        | 10.06         |
| micro                    | 9.4.1   | ✗      | 55964.8    | 17.37        | 9.98          |
| restana                  | 4.9.7   | ✓      | 54652.8    | 17.79        | 9.75          |
| server-base              | 7.1.32  | ✗      | 54468.0    | 17.87        | 9.71          |
| fastify                  | 4.26.2  | ✓      | 54394.4    | 17.89        | 9.75          |
| server-base-router       | 7.1.32  | ✓      | 53027.2    | 18.36        | 9.46          |
| yeps                     | 1.1.1   | ✗      | 51607.2    | 18.88        | 9.20          |
| connect-router           | 1.3.8   | ✓      | 50223.2    | 19.42        | 8.96          |
| micro-route              | 2.5.0   | ✓      | 49930.4    | 19.53        | 8.90          |
| trek-engine              | 1.0.5   | ✗      | 48080.8    | 20.30        | 7.89          |
| trek-router              | 1.2.0   | ✓      | 47430.4    | 20.58        | 7.78          |
| vapr                     | 0.6.0   | ✓      | 45329.6    | 21.55        | 7.44          |
| yeps-router              | 1.2.0   | ✓      | 44502.4    | 21.98        | 7.94          |
| spirit-router            | 0.5.0   | ✓      | 42749.6    | 22.88        | 7.62          |
| koa                      | 2.15.2  | ✗      | 41989.8    | 23.32        | 7.49          |
| spirit                   | 0.6.1   | ✗      | 41772.0    | 23.45        | 7.45          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40138.2    | 24.42        | 7.16          |
| restify                  | 8.6.1   | ✓      | 38332.6    | 25.58        | 6.91          |
| take-five                | 2.0.0   | ✓      | 38254.2    | 25.64        | 13.75         |
| total.js                 | 3.4.13  | ✓      | 37895.0    | 25.89        | 11.60         |
| koa-router               | 12.0.1  | ✓      | 36647.8    | 26.79        | 6.53          |
| hapi                     | 20.3.0  | ✓      | 33328.8    | 29.50        | 5.94          |
| microrouter              | 3.1.3   | ✓      | 31992.4    | 30.75        | 5.71          |
| trpc-router              | 9.27.4  | ✓      | 26263.2    | 37.56        | 5.81          |
| egg.js                   | 3.21.0  | ✓      | 17317.5    | 57.23        | 6.19          |
| express                  | 4.19.2  | ✓      | 13438.4    | 73.86        | 2.40          |
| fastify-big-json         | 4.26.2  | ✓      | 12761.4    | 77.82        | 146.83        |
| express-with-middlewares | 4.19.2  | ✓      | 12441.4    | 79.83        | 4.63          |
| express-route-prefix     | 4.19.2  | ✓      | 11075.8    | 89.73        | 4.10          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

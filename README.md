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
* __Run:__ Mon Feb 19 2024 02:07:35 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68074.4    | 14.20        | 12.14         |
| h3                       | 0.8.6   | ✗      | 63929.2    | 15.16        | 10.49         |
| h3-router                | 0.8.6   | ✓      | 61228.8    | 15.83        | 10.04         |
| 0http                    | 3.5.2   | ✓      | 60129.6    | 16.13        | 10.72         |
| bare                     | 10.13.0 | ✗      | 59912.0    | 16.19        | 10.68         |
| foxify                   | 0.10.20 | ✓      | 58362.4    | 16.64        | 9.57          |
| polka                    | 0.5.2   | ✓      | 57209.6    | 16.99        | 10.20         |
| connect                  | 3.7.0   | ✗      | 56528.8    | 17.20        | 10.08         |
| restana                  | 4.9.7   | ✓      | 54936.8    | 17.71        | 9.80          |
| micro                    | 9.4.1   | ✗      | 54891.2    | 17.72        | 9.79          |
| server-base-router       | 7.1.32  | ✓      | 54798.4    | 17.75        | 9.77          |
| fastify                  | 4.26.1  | ✓      | 54726.4    | 17.77        | 9.81          |
| server-base              | 7.1.32  | ✗      | 52623.2    | 18.51        | 9.38          |
| yeps                     | 1.1.1   | ✗      | 51032.8    | 19.09        | 9.10          |
| connect-router           | 1.3.8   | ✓      | 48874.4    | 19.96        | 8.72          |
| micro-route              | 2.5.0   | ✓      | 48484.8    | 20.13        | 8.65          |
| trek-engine              | 1.0.5   | ✗      | 48391.2    | 20.17        | 7.94          |
| trek-router              | 1.2.0   | ✓      | 47127.2    | 20.72        | 7.73          |
| vapr                     | 0.6.0   | ✓      | 45298.4    | 21.57        | 7.43          |
| yeps-router              | 1.2.0   | ✓      | 43990.4    | 22.23        | 7.85          |
| spirit-router            | 0.5.0   | ✓      | 41241.6    | 23.76        | 7.35          |
| spirit                   | 0.6.1   | ✗      | 41174.4    | 23.79        | 7.34          |
| koa                      | 2.15.0  | ✗      | 40610.4    | 24.12        | 7.24          |
| total.js                 | 3.4.13  | ✓      | 39486.4    | 24.83        | 12.09         |
| restify                  | 8.6.1   | ✓      | 38855.4    | 25.24        | 7.00          |
| take-five                | 2.0.0   | ✓      | 38579.0    | 25.42        | 13.87         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37505.0    | 26.16        | 6.69          |
| koa-router               | 12.0.1  | ✓      | 35564.2    | 27.62        | 6.34          |
| hapi                     | 20.3.0  | ✓      | 33863.0    | 29.03        | 6.04          |
| microrouter              | 3.1.3   | ✓      | 32564.4    | 30.20        | 5.81          |
| trpc-router              | 9.27.4  | ✓      | 27083.6    | 36.41        | 5.99          |
| egg.js                   | 3.19.0  | ✓      | 16988.1    | 58.34        | 6.08          |
| express                  | 4.18.2  | ✓      | 13224.2    | 75.07        | 2.36          |
| fastify-big-json         | 4.26.1  | ✓      | 12575.4    | 78.98        | 144.69        |
| express-with-middlewares | 4.18.2  | ✓      | 12539.4    | 79.19        | 4.66          |
| express-route-prefix     | 4.18.2  | ✓      | 11044.6    | 89.96        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

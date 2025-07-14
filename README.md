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
* __Run:__ Mon Jul 14 2025 03:15:23 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67658.4    | 14.27        | 12.07         |
| polkadot                 | 1.0.0   | ✗      | 67502.0    | 14.32        | 12.04         |
| h3                       | 0.8.6   | ✗      | 65552.8    | 14.77        | 10.75         |
| h3-router                | 0.8.6   | ✓      | 62412.0    | 15.50        | 10.24         |
| bare                     | 10.13.0 | ✗      | 60899.2    | 15.93        | 10.86         |
| foxify                   | 0.10.20 | ✓      | 60212.8    | 16.11        | 9.88          |
| restana                  | 4.9.9   | ✓      | 59546.4    | 16.29        | 10.62         |
| connect                  | 3.7.0   | ✗      | 57527.2    | 16.88        | 10.26         |
| polka                    | 0.5.2   | ✓      | 56784.0    | 17.11        | 10.13         |
| fastify                  | 4.29.1  | ✓      | 55194.4    | 17.62        | 9.90          |
| micro                    | 9.4.1   | ✗      | 54676.8    | 17.79        | 9.75          |
| server-base              | 7.1.32  | ✗      | 54000.8    | 18.02        | 9.63          |
| server-base-router       | 7.1.32  | ✓      | 53784.8    | 18.10        | 9.59          |
| yeps                     | 1.1.1   | ✗      | 53261.6    | 18.28        | 9.50          |
| connect-router           | 1.3.8   | ✓      | 50512.8    | 19.30        | 9.01          |
| micro-route              | 2.5.0   | ✓      | 50192.0    | 19.42        | 8.95          |
| trek-engine              | 1.0.5   | ✗      | 47868.8    | 20.39        | 7.85          |
| trek-router              | 1.2.0   | ✓      | 45497.6    | 21.48        | 7.46          |
| vapr                     | 0.6.0   | ✓      | 44806.4    | 21.82        | 7.35          |
| spirit                   | 0.6.1   | ✗      | 43217.6    | 22.64        | 7.71          |
| yeps-router              | 1.2.0   | ✓      | 42964.0    | 22.77        | 7.66          |
| koa                      | 2.16.1  | ✗      | 42741.6    | 22.89        | 7.62          |
| spirit-router            | 0.5.0   | ✓      | 41047.2    | 23.86        | 7.32          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39433.4    | 24.85        | 7.03          |
| total.js                 | 3.4.13  | ✓      | 39284.8    | 24.95        | 12.03         |
| take-five                | 2.0.0   | ✓      | 38417.8    | 25.52        | 13.81         |
| restify                  | 8.6.1   | ✓      | 37521.0    | 26.15        | 6.76          |
| koa-router               | 12.0.1  | ✓      | 36427.4    | 26.96        | 6.50          |
| hapi                     | 20.3.0  | ✓      | 33452.2    | 29.40        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 31170.8    | 31.57        | 5.56          |
| trpc-router              | 9.27.4  | ✓      | 26451.6    | 37.30        | 5.85          |
| egg.js                   | 3.31.0  | ✓      | 16659.0    | 59.49        | 5.96          |
| express                  | 4.21.2  | ✓      | 13248.8    | 74.94        | 2.36          |
| fastify-big-json         | 4.29.1  | ✓      | 12927.2    | 76.81        | 148.73        |
| express-with-middlewares | 4.21.2  | ✓      | 12212.4    | 81.32        | 4.54          |
| express-route-prefix     | 4.21.2  | ✓      | 10925.0    | 90.98        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon May 19 2025 03:00:32 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69833.2    | 13.83        | 12.45         |
| h3                       | 0.8.6   | ✗      | 67524.0    | 14.33        | 11.08         |
| polkadot                 | 1.0.0   | ✗      | 67136.0    | 14.40        | 11.97         |
| h3-router                | 0.8.6   | ✓      | 66634.0    | 14.50        | 10.93         |
| restana                  | 4.9.9   | ✓      | 62658.4    | 15.45        | 11.17         |
| bare                     | 10.13.0 | ✗      | 59704.0    | 16.25        | 10.65         |
| foxify                   | 0.10.20 | ✓      | 58285.6    | 16.66        | 9.56          |
| polka                    | 0.5.2   | ✓      | 56620.0    | 17.16        | 10.10         |
| connect                  | 3.7.0   | ✗      | 56256.0    | 17.28        | 10.03         |
| micro                    | 9.4.1   | ✗      | 56243.2    | 17.28        | 10.03         |
| fastify                  | 4.29.1  | ✓      | 56222.4    | 17.29        | 10.08         |
| server-base              | 7.1.32  | ✗      | 54659.2    | 17.79        | 9.75          |
| server-base-router       | 7.1.32  | ✓      | 54570.4    | 17.82        | 9.73          |
| yeps                     | 1.1.1   | ✗      | 51548.0    | 18.90        | 9.19          |
| connect-router           | 1.3.8   | ✓      | 50497.6    | 19.30        | 9.01          |
| micro-route              | 2.5.0   | ✓      | 49148.8    | 19.85        | 8.76          |
| trek-engine              | 1.0.5   | ✗      | 48708.8    | 20.03        | 7.99          |
| trek-router              | 1.2.0   | ✓      | 48294.4    | 20.21        | 7.92          |
| vapr                     | 0.6.0   | ✓      | 45612.8    | 21.42        | 7.48          |
| spirit-router            | 0.5.0   | ✓      | 43141.6    | 22.67        | 7.69          |
| yeps-router              | 1.2.0   | ✓      | 43131.2    | 22.67        | 7.69          |
| koa                      | 2.16.1  | ✗      | 42702.4    | 22.91        | 7.62          |
| spirit                   | 0.6.1   | ✗      | 42529.6    | 23.01        | 7.58          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39568.6    | 24.78        | 7.06          |
| take-five                | 2.0.0   | ✓      | 39091.0    | 25.08        | 14.06         |
| restify                  | 8.6.1   | ✓      | 38953.0    | 25.16        | 7.02          |
| total.js                 | 3.4.13  | ✓      | 38859.2    | 25.24        | 11.90         |
| koa-router               | 12.0.1  | ✓      | 36414.6    | 26.96        | 6.49          |
| hapi                     | 20.3.0  | ✓      | 33561.0    | 29.30        | 5.98          |
| microrouter              | 3.1.3   | ✓      | 31781.6    | 30.96        | 5.67          |
| trpc-router              | 9.27.4  | ✓      | 27354.8    | 36.05        | 6.05          |
| egg.js                   | 3.30.1  | ✓      | 17605.3    | 56.27        | 6.30          |
| express                  | 4.21.2  | ✓      | 13563.6    | 73.19        | 2.42          |
| fastify-big-json         | 4.29.1  | ✓      | 12767.8    | 77.76        | 146.90        |
| express-with-middlewares | 4.21.2  | ✓      | 12278.6    | 80.89        | 4.57          |
| express-route-prefix     | 4.21.2  | ✓      | 10968.2    | 90.58        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon May 29 2023 02:32:07 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 63195.2    | 15.29        | 11.27         |
| 0http                    | 3.5.2   | ✓      | 62073.6    | 15.59        | 11.07         |
| h3-router                | 0.8.6   | ✓      | 61243.2    | 15.83        | 10.05         |
| h3                       | 0.8.6   | ✗      | 61109.6    | 15.87        | 10.02         |
| bare                     | 10.13.0 | ✗      | 60692.8    | 15.99        | 10.82         |
| polka                    | 0.5.2   | ✓      | 60160.8    | 16.13        | 10.73         |
| fastify                  | 4.17.0  | ✓      | 59695.2    | 16.25        | 10.70         |
| foxify                   | 0.10.20 | ✓      | 59432.0    | 16.33        | 9.75          |
| micro                    | 9.4.1   | ✗      | 57772.0    | 16.81        | 10.30         |
| connect                  | 3.7.0   | ✗      | 57093.8    | 17.02        | 10.18         |
| server-base-router       | 7.1.32  | ✓      | 56186.4    | 17.30        | 10.02         |
| restana                  | 4.9.7   | ✓      | 56093.6    | 17.29        | 10.00         |
| server-base              | 7.1.32  | ✗      | 55399.2    | 17.55        | 9.88          |
| yeps                     | 1.1.1   | ✗      | 55110.4    | 17.65        | 9.83          |
| connect-router           | 1.3.8   | ✓      | 53441.6    | 18.22        | 9.53          |
| micro-route              | 2.5.0   | ✓      | 51489.6    | 18.91        | 9.18          |
| trek-engine              | 1.0.5   | ✗      | 51048.8    | 19.09        | 8.37          |
| vapr                     | 0.6.0   | ✓      | 49180.8    | 19.84        | 8.07          |
| trek-router              | 1.2.0   | ✓      | 48953.0    | 19.94        | 8.03          |
| spirit                   | 0.6.1   | ✗      | 44844.8    | 21.80        | 8.00          |
| koa                      | 2.14.2  | ✗      | 44476.8    | 22.00        | 7.93          |
| yeps-router              | 1.2.0   | ✓      | 43916.0    | 22.27        | 7.83          |
| spirit-router            | 0.5.0   | ✓      | 43073.6    | 22.72        | 7.68          |
| take-five                | 2.0.0   | ✓      | 41755.0    | 23.44        | 15.01         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41429.6    | 23.66        | 7.39          |
| total.js                 | 3.4.13  | ✓      | 40775.2    | 24.02        | 12.48         |
| restify                  | 8.6.1   | ✓      | 39993.0    | 24.49        | 7.21          |
| koa-router               | 12.0.0  | ✓      | 38327.0    | 25.60        | 6.83          |
| hapi                     | 20.3.0  | ✓      | 34554.2    | 28.44        | 6.16          |
| microrouter              | 3.1.3   | ✓      | 33003.0    | 29.81        | 5.89          |
| trpc-router              | 9.27.3  | ✓      | 28492.8    | 34.59        | 6.30          |
| egg.js                   | 3.16.0  | ✓      | 16974.5    | 58.37        | 6.07          |
| express                  | 4.18.2  | ✓      | 13806.2    | 71.88        | 2.46          |
| express-with-middlewares | 4.18.2  | ✓      | 12354.8    | 80.41        | 4.60          |
| fastify-big-json         | 4.17.0  | ✓      | 11858.0    | 83.78        | 136.44        |
| express-route-prefix     | 4.18.2  | ✓      | 11768.0    | 84.41        | 4.35          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

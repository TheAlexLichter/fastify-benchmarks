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
* __Node:__ `v14.21.1`
* __Run:__ Mon Dec 05 2022 02:34:50 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 62242.4    | 15.57        | 11.10         |
| bare                     | 10.13.0 | ✗      | 60839.2    | 15.95        | 10.85         |
| 0http                    | 3.4.1   | ✓      | 60636.8    | 16.01        | 10.81         |
| foxify                   | 0.10.20 | ✓      | 60456.8    | 16.04        | 9.92          |
| h3                       | 0.8.6   | ✗      | 60296.0    | 16.08        | 9.89          |
| polka                    | 0.5.2   | ✓      | 60117.6    | 16.14        | 10.72         |
| fastify                  | 4.10.2  | ✓      | 59566.4    | 16.28        | 10.68         |
| micro                    | 9.4.1   | ✗      | 58388.0    | 16.61        | 10.41         |
| connect                  | 3.7.0   | ✗      | 58092.8    | 16.72        | 10.36         |
| server-base              | 7.1.32  | ✗      | 57294.4    | 16.96        | 10.22         |
| h3-router                | 0.8.6   | ✓      | 56959.2    | 17.07        | 9.34          |
| server-base-router       | 7.1.32  | ✓      | 55840.0    | 17.41        | 9.96          |
| restana                  | 4.9.6   | ✓      | 54960.0    | 17.68        | 9.80          |
| yeps                     | 1.1.1   | ✗      | 54719.2    | 17.78        | 9.76          |
| connect-router           | 1.3.7   | ✓      | 53388.8    | 18.24        | 9.52          |
| micro-route              | 2.5.0   | ✓      | 52971.2    | 18.38        | 9.45          |
| trek-router              | 1.2.0   | ✓      | 50500.8    | 19.31        | 8.28          |
| vapr                     | 0.6.0   | ✓      | 49209.6    | 19.83        | 8.07          |
| trek-engine              | 1.0.5   | ✗      | 48582.2    | 20.09        | 7.97          |
| spirit                   | 0.6.1   | ✗      | 46320.0    | 21.10        | 8.26          |
| yeps-router              | 1.2.0   | ✓      | 44816.8    | 21.81        | 7.99          |
| spirit-router            | 0.5.0   | ✓      | 44386.4    | 22.04        | 7.92          |
| koa                      | 2.13.4  | ✗      | 43762.4    | 22.34        | 7.80          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41549.8    | 23.57        | 7.41          |
| take-five                | 2.0.0   | ✓      | 41204.6    | 23.77        | 14.81         |
| total.js                 | 3.4.13  | ✓      | 40463.8    | 24.20        | 12.39         |
| restify                  | 8.6.1   | ✓      | 38346.6    | 25.57        | 6.91          |
| koa-router               | 12.0.0  | ✓      | 36930.6    | 26.57        | 6.59          |
| hapi                     | 20.2.2  | ✓      | 34129.2    | 28.80        | 6.09          |
| microrouter              | 3.1.3   | ✓      | 32697.8    | 30.08        | 5.83          |
| trpc-router              | 9.27.4  | ✓      | 28380.0    | 34.73        | 6.28          |
| egg.js                   | 3.5.0   | ✓      | 19550.8    | 50.64        | 6.99          |
| express                  | 4.18.2  | ✓      | 13712.8    | 72.40        | 2.45          |
| express-with-middlewares | 4.18.2  | ✓      | 12401.6    | 80.06        | 4.61          |
| express-route-prefix     | 4.18.2  | ✓      | 12137.0    | 81.82        | 4.49          |
| fastify-big-json         | 4.10.2  | ✓      | 11375.8    | 87.46        | 130.88        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

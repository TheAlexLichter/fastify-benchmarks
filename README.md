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
* __Run:__ Mon Nov 06 2023 02:10:47 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67274.4    | 14.37        | 12.00         |
| h3                       | 0.8.6   | ✗      | 65759.6    | 14.71        | 10.79         |
| 0http                    | 3.5.2   | ✓      | 64618.8    | 14.98        | 11.52         |
| h3-router                | 0.8.6   | ✓      | 64616.8    | 14.99        | 10.60         |
| bare                     | 10.13.0 | ✗      | 58986.4    | 16.45        | 10.52         |
| polka                    | 0.5.2   | ✓      | 56346.4    | 17.25        | 10.05         |
| foxify                   | 0.10.20 | ✓      | 56224.8    | 17.28        | 9.22          |
| fastify                  | 4.24.3  | ✓      | 55153.6    | 17.64        | 9.89          |
| restana                  | 4.9.7   | ✓      | 55145.6    | 17.64        | 9.83          |
| micro                    | 9.4.1   | ✗      | 54735.2    | 17.77        | 9.76          |
| connect                  | 3.7.0   | ✗      | 54465.6    | 17.87        | 9.71          |
| server-base-router       | 7.1.32  | ✓      | 53908.0    | 18.05        | 9.61          |
| server-base              | 7.1.32  | ✗      | 53332.8    | 18.25        | 9.51          |
| yeps                     | 1.1.1   | ✗      | 50409.6    | 19.34        | 8.99          |
| connect-router           | 1.3.8   | ✓      | 49060.0    | 19.89        | 8.75          |
| micro-route              | 2.5.0   | ✓      | 48360.0    | 20.18        | 8.62          |
| trek-engine              | 1.0.5   | ✗      | 47053.6    | 20.75        | 7.72          |
| trek-router              | 1.2.0   | ✓      | 46963.2    | 20.80        | 7.70          |
| vapr                     | 0.6.0   | ✓      | 45824.8    | 21.32        | 7.52          |
| spirit                   | 0.6.1   | ✗      | 43709.6    | 22.35        | 7.80          |
| yeps-router              | 1.2.0   | ✓      | 42620.0    | 22.98        | 7.60          |
| koa                      | 2.14.2  | ✗      | 42021.6    | 23.30        | 7.49          |
| spirit-router            | 0.5.0   | ✓      | 41710.4    | 23.49        | 7.44          |
| restify                  | 8.6.1   | ✓      | 38756.2    | 25.31        | 6.99          |
| take-five                | 2.0.0   | ✓      | 38450.6    | 25.51        | 13.82         |
| total.js                 | 3.4.13  | ✓      | 38275.2    | 25.62        | 11.72         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38099.8    | 25.75        | 6.79          |
| koa-router               | 12.0.1  | ✓      | 36219.4    | 27.11        | 6.46          |
| hapi                     | 20.3.0  | ✓      | 32810.2    | 29.97        | 5.85          |
| microrouter              | 3.1.3   | ✓      | 30779.2    | 31.99        | 5.49          |
| trpc-router              | 9.27.3  | ✓      | 26382.0    | 37.40        | 5.84          |
| egg.js                   | 3.17.5  | ✓      | 17410.5    | 56.92        | 6.23          |
| express                  | 4.18.2  | ✓      | 13417.2    | 73.98        | 2.39          |
| fastify-big-json         | 4.24.3  | ✓      | 12828.2    | 77.43        | 147.59        |
| express-with-middlewares | 4.18.2  | ✓      | 12446.4    | 79.80        | 4.63          |
| express-route-prefix     | 4.18.2  | ✓      | 10991.8    | 90.39        | 4.07          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jun 02 2025 03:02:39 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69416.0    | 13.90        | 12.38         |
| polkadot                 | 1.0.0   | ✗      | 68392.4    | 14.13        | 12.20         |
| h3                       | 0.8.6   | ✗      | 65774.4    | 14.70        | 10.79         |
| h3-router                | 0.8.6   | ✓      | 65020.4    | 14.89        | 10.67         |
| restana                  | 4.9.9   | ✓      | 60748.0    | 15.97        | 10.83         |
| bare                     | 10.13.0 | ✗      | 60116.0    | 16.12        | 10.72         |
| foxify                   | 0.10.20 | ✓      | 59663.2    | 16.26        | 9.79          |
| polka                    | 0.5.2   | ✓      | 57917.6    | 16.76        | 10.33         |
| connect                  | 3.7.0   | ✗      | 57246.4    | 16.97        | 10.21         |
| micro                    | 9.4.1   | ✗      | 57012.0    | 17.05        | 10.17         |
| fastify                  | 4.29.1  | ✓      | 55299.2    | 17.59        | 9.91          |
| server-base              | 7.1.32  | ✗      | 54500.0    | 17.85        | 9.72          |
| server-base-router       | 7.1.32  | ✓      | 54368.0    | 17.90        | 9.70          |
| yeps                     | 1.1.1   | ✗      | 51435.2    | 18.95        | 9.17          |
| connect-router           | 1.3.8   | ✓      | 51170.4    | 19.04        | 9.13          |
| micro-route              | 2.5.0   | ✓      | 50156.0    | 19.45        | 8.95          |
| trek-engine              | 1.0.5   | ✗      | 49242.4    | 19.82        | 8.08          |
| trek-router              | 1.2.0   | ✓      | 47452.8    | 20.58        | 7.78          |
| vapr                     | 0.6.0   | ✓      | 45922.4    | 21.28        | 7.53          |
| yeps-router              | 1.2.0   | ✓      | 44514.4    | 21.97        | 7.94          |
| koa                      | 2.16.1  | ✗      | 42505.8    | 23.04        | 7.58          |
| spirit                   | 0.6.1   | ✗      | 41204.8    | 23.78        | 7.35          |
| total.js                 | 3.4.13  | ✓      | 39335.2    | 24.92        | 12.04         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39166.2    | 25.03        | 6.98          |
| restify                  | 8.6.1   | ✓      | 38687.0    | 25.34        | 6.97          |
| take-five                | 2.0.0   | ✓      | 37395.4    | 26.25        | 13.44         |
| koa-router               | 12.0.1  | ✓      | 36990.6    | 26.54        | 6.60          |
| spirit-router            | 0.5.0   | ✓      | 36543.2    | 26.86        | 6.52          |
| hapi                     | 20.3.0  | ✓      | 34461.0    | 28.51        | 6.15          |
| microrouter              | 3.1.3   | ✓      | 32086.4    | 30.66        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 27570.4    | 35.76        | 6.10          |
| egg.js                   | 3.30.1  | ✓      | 17601.0    | 56.30        | 6.29          |
| express                  | 4.21.2  | ✓      | 13689.8    | 72.51        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12851.8    | 77.28        | 147.87        |
| express-with-middlewares | 4.21.2  | ✓      | 12533.0    | 79.23        | 4.66          |
| express-route-prefix     | 4.21.2  | ✓      | 11000.0    | 90.32        | 4.07          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

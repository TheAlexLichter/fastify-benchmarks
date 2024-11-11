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
* __Run:__ Mon Nov 11 2024 02:38:31 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69389.6    | 13.91        | 12.38         |
| polkadot                 | 1.0.0   | ✗      | 68649.6    | 14.07        | 12.24         |
| h3-router                | 0.8.6   | ✓      | 65557.6    | 14.76        | 10.75         |
| h3                       | 0.8.6   | ✗      | 65544.8    | 14.76        | 10.75         |
| bare                     | 10.13.0 | ✗      | 60695.2    | 15.99        | 10.82         |
| restana                  | 4.9.9   | ✓      | 59992.8    | 16.20        | 10.70         |
| polka                    | 0.5.2   | ✓      | 59308.8    | 16.36        | 10.58         |
| foxify                   | 0.10.20 | ✓      | 59171.2    | 16.40        | 9.71          |
| micro                    | 9.4.1   | ✗      | 57273.6    | 16.97        | 10.21         |
| connect                  | 3.7.0   | ✗      | 57259.2    | 16.98        | 10.21         |
| fastify                  | 4.28.1  | ✓      | 56132.0    | 17.31        | 10.06         |
| server-base-router       | 7.1.32  | ✓      | 55411.2    | 17.55        | 9.88          |
| server-base              | 7.1.32  | ✗      | 55180.8    | 17.63        | 9.84          |
| yeps                     | 1.1.1   | ✗      | 53433.6    | 18.22        | 9.53          |
| connect-router           | 1.3.8   | ✓      | 50636.8    | 19.25        | 9.03          |
| micro-route              | 2.5.0   | ✓      | 50550.4    | 19.29        | 9.02          |
| trek-engine              | 1.0.5   | ✗      | 49823.2    | 19.58        | 8.17          |
| trek-router              | 1.2.0   | ✓      | 47654.4    | 20.49        | 7.82          |
| vapr                     | 0.6.0   | ✓      | 46894.4    | 20.83        | 7.69          |
| spirit                   | 0.6.1   | ✗      | 44671.2    | 21.91        | 7.97          |
| yeps-router              | 1.2.0   | ✓      | 43785.6    | 22.33        | 7.81          |
| spirit-router            | 0.5.0   | ✓      | 43145.6    | 22.65        | 7.69          |
| koa                      | 2.15.3  | ✗      | 43124.2    | 22.70        | 7.69          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40620.0    | 24.12        | 7.24          |
| total.js                 | 3.4.13  | ✓      | 39859.2    | 24.59        | 12.20         |
| restify                  | 8.6.1   | ✓      | 39343.0    | 24.93        | 7.09          |
| take-five                | 2.0.0   | ✓      | 39254.6    | 24.97        | 14.11         |
| koa-router               | 12.0.1  | ✓      | 38071.4    | 25.76        | 6.79          |
| hapi                     | 20.3.0  | ✓      | 34194.0    | 28.74        | 6.10          |
| microrouter              | 3.1.3   | ✓      | 31842.4    | 30.90        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 26673.2    | 36.98        | 5.90          |
| egg.js                   | 3.28.0  | ✓      | 17306.3    | 57.28        | 6.19          |
| express                  | 4.21.1  | ✓      | 13505.0    | 73.48        | 2.41          |
| fastify-big-json         | 4.28.1  | ✓      | 12995.6    | 76.42        | 149.52        |
| express-with-middlewares | 4.21.1  | ✓      | 12688.2    | 78.26        | 4.72          |
| express-route-prefix     | 4.21.1  | ✓      | 10932.2    | 90.89        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

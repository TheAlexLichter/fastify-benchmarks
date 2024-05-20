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
* __Run:__ Mon May 20 2024 02:12:59 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67890.4    | 14.23        | 12.11         |
| polkadot                 | 1.0.0   | ✗      | 65933.2    | 14.68        | 11.76         |
| h3                       | 0.8.6   | ✗      | 64220.4    | 15.07        | 10.53         |
| bare                     | 10.13.0 | ✗      | 61669.6    | 15.74        | 11.00         |
| h3-router                | 0.8.6   | ✓      | 60818.4    | 15.96        | 9.98          |
| restana                  | 4.9.9   | ✓      | 60680.8    | 15.99        | 10.82         |
| foxify                   | 0.10.20 | ✓      | 58962.4    | 16.46        | 9.67          |
| polka                    | 0.5.2   | ✓      | 58230.4    | 16.68        | 10.38         |
| connect                  | 3.7.0   | ✗      | 57591.2    | 16.87        | 10.27         |
| fastify                  | 4.27.0  | ✓      | 57329.6    | 16.95        | 10.28         |
| micro                    | 9.4.1   | ✗      | 56916.0    | 17.07        | 10.15         |
| server-base-router       | 7.1.32  | ✓      | 54912.8    | 17.71        | 9.79          |
| server-base              | 7.1.32  | ✗      | 52757.6    | 18.46        | 9.41          |
| yeps                     | 1.1.1   | ✗      | 52648.0    | 18.50        | 9.39          |
| micro-route              | 2.5.0   | ✓      | 49984.0    | 19.50        | 8.91          |
| connect-router           | 1.3.8   | ✓      | 49983.2    | 19.51        | 8.91          |
| trek-router              | 1.2.0   | ✓      | 48856.0    | 19.97        | 8.01          |
| trek-engine              | 1.0.5   | ✗      | 48564.8    | 20.09        | 7.97          |
| vapr                     | 0.6.0   | ✓      | 46640.8    | 20.94        | 7.65          |
| yeps-router              | 1.2.0   | ✓      | 44626.4    | 21.92        | 7.96          |
| spirit                   | 0.6.1   | ✗      | 43395.2    | 22.49        | 7.74          |
| koa                      | 2.15.3  | ✗      | 43091.2    | 22.70        | 7.68          |
| spirit-router            | 0.5.0   | ✓      | 41944.8    | 23.37        | 7.48          |
| restify                  | 8.6.1   | ✓      | 39952.0    | 24.52        | 7.20          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39813.8    | 24.62        | 7.10          |
| total.js                 | 3.4.13  | ✓      | 39201.0    | 25.02        | 12.00         |
| take-five                | 2.0.0   | ✓      | 39125.4    | 25.07        | 14.07         |
| koa-router               | 12.0.1  | ✓      | 37041.0    | 26.50        | 6.61          |
| hapi                     | 20.3.0  | ✓      | 33892.6    | 29.01        | 6.04          |
| microrouter              | 3.1.3   | ✓      | 32285.0    | 30.46        | 5.76          |
| trpc-router              | 9.27.4  | ✓      | 26359.6    | 37.43        | 5.83          |
| egg.js                   | 3.23.0  | ✓      | 17544.4    | 56.46        | 6.27          |
| express                  | 4.19.2  | ✓      | 14382.6    | 69.00        | 2.56          |
| fastify-big-json         | 4.27.0  | ✓      | 12809.6    | 77.52        | 147.39        |
| express-with-middlewares | 4.19.2  | ✓      | 12652.6    | 78.47        | 4.71          |
| express-route-prefix     | 4.19.2  | ✓      | 11016.4    | 90.20        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

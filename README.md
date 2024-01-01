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
* __Run:__ Mon Jan 01 2024 02:23:45 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 66757.2    | 14.49        | 11.91         |
| h3-router                | 0.8.6   | ✓      | 65537.2    | 14.76        | 10.75         |
| 0http                    | 3.5.2   | ✓      | 64475.2    | 15.01        | 11.50         |
| h3                       | 0.8.6   | ✗      | 63731.2    | 15.20        | 10.45         |
| bare                     | 10.13.0 | ✗      | 60798.4    | 15.95        | 10.84         |
| foxify                   | 0.10.20 | ✓      | 59916.8    | 16.19        | 9.83          |
| polka                    | 0.5.2   | ✓      | 58232.8    | 16.68        | 10.38         |
| fastify                  | 4.25.2  | ✓      | 57199.2    | 16.99        | 10.26         |
| micro                    | 9.4.1   | ✗      | 56519.2    | 17.20        | 10.08         |
| connect                  | 3.7.0   | ✗      | 56342.4    | 17.24        | 10.05         |
| restana                  | 4.9.7   | ✓      | 55716.8    | 17.44        | 9.94          |
| server-base-router       | 7.1.32  | ✓      | 55628.0    | 17.47        | 9.92          |
| server-base              | 7.1.32  | ✗      | 54980.0    | 17.70        | 9.80          |
| yeps                     | 1.1.1   | ✗      | 52032.8    | 18.72        | 9.28          |
| micro-route              | 2.5.0   | ✓      | 49688.0    | 19.64        | 8.86          |
| connect-router           | 1.3.8   | ✓      | 48972.0    | 19.93        | 8.73          |
| trek-engine              | 1.0.5   | ✗      | 48835.2    | 19.98        | 8.01          |
| trek-router              | 1.2.0   | ✓      | 48204.8    | 20.25        | 7.91          |
| vapr                     | 0.6.0   | ✓      | 45679.2    | 21.38        | 7.49          |
| yeps-router              | 1.2.0   | ✓      | 44141.4    | 22.16        | 7.87          |
| spirit                   | 0.6.1   | ✗      | 44069.6    | 22.23        | 7.86          |
| koa                      | 2.15.0  | ✗      | 43022.4    | 22.76        | 7.67          |
| spirit-router            | 0.5.0   | ✓      | 42018.4    | 23.29        | 7.49          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39842.4    | 24.60        | 7.11          |
| total.js                 | 3.4.13  | ✓      | 39758.4    | 24.67        | 12.17         |
| restify                  | 8.6.1   | ✓      | 39276.6    | 24.96        | 7.08          |
| take-five                | 2.0.0   | ✓      | 39056.6    | 25.09        | 14.04         |
| koa-router               | 12.0.1  | ✓      | 37733.0    | 26.00        | 6.73          |
| hapi                     | 20.3.0  | ✓      | 34047.8    | 28.85        | 6.07          |
| microrouter              | 3.1.3   | ✓      | 31898.0    | 30.84        | 5.69          |
| trpc-router              | 9.27.4  | ✓      | 27071.2    | 36.43        | 5.99          |
| egg.js                   | 3.17.5  | ✓      | 17548.3    | 56.46        | 6.28          |
| express                  | 4.18.2  | ✓      | 13595.2    | 72.99        | 2.42          |
| fastify-big-json         | 4.25.2  | ✓      | 13024.8    | 76.26        | 149.86        |
| express-with-middlewares | 4.18.2  | ✓      | 12530.8    | 79.25        | 4.66          |
| express-route-prefix     | 4.18.2  | ✓      | 11178.2    | 88.87        | 4.14          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

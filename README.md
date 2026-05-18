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
* __Run:__ Mon May 18 2026 05:12:07 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68690.8    | 14.06        | 12.25         |
| polkadot                 | 1.0.0   | ✗      | 67650.0    | 14.29        | 12.07         |
| h3-router                | 0.8.6   | ✓      | 65442.0    | 14.79        | 10.73         |
| h3                       | 0.8.6   | ✗      | 65290.0    | 14.82        | 10.71         |
| restana                  | 4.9.9   | ✓      | 60835.2    | 15.97        | 10.85         |
| bare                     | 10.13.0 | ✗      | 59912.8    | 16.20        | 10.68         |
| foxify                   | 0.10.20 | ✓      | 58921.6    | 16.47        | 9.67          |
| polka                    | 0.5.2   | ✓      | 58419.2    | 16.62        | 10.42         |
| micro                    | 9.4.1   | ✗      | 58057.6    | 16.73        | 10.35         |
| fastify                  | 4.29.1  | ✓      | 57380.0    | 16.93        | 10.29         |
| connect                  | 3.7.0   | ✗      | 56956.8    | 17.06        | 10.16         |
| server-base              | 7.1.32  | ✗      | 54560.8    | 17.83        | 9.73          |
| server-base-router       | 7.1.32  | ✓      | 53504.0    | 18.18        | 9.54          |
| yeps                     | 1.1.1   | ✗      | 51838.4    | 18.80        | 9.24          |
| connect-router           | 1.3.8   | ✓      | 51198.4    | 19.05        | 9.13          |
| micro-route              | 2.5.0   | ✓      | 49807.2    | 19.57        | 8.88          |
| trek-engine              | 1.0.5   | ✗      | 48248.8    | 20.24        | 7.91          |
| trek-router              | 1.2.0   | ✓      | 47804.8    | 20.42        | 7.84          |
| vapr                     | 0.6.0   | ✓      | 46173.6    | 21.16        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 44264.8    | 22.10        | 7.89          |
| yeps-router              | 1.2.0   | ✓      | 43326.4    | 22.58        | 7.73          |
| spirit-router            | 0.5.0   | ✓      | 42624.0    | 22.98        | 7.60          |
| koa                      | 2.16.4  | ✗      | 41660.0    | 23.50        | 7.43          |
| total.js                 | 3.4.13  | ✓      | 39640.0    | 24.72        | 12.14         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38667.8    | 25.35        | 6.90          |
| take-five                | 2.0.0   | ✓      | 38220.6    | 25.66        | 13.74         |
| restify                  | 8.6.1   | ✓      | 38096.2    | 25.75        | 6.87          |
| koa-router               | 12.0.1  | ✓      | 36450.2    | 26.93        | 6.50          |
| hapi                     | 20.3.0  | ✓      | 32488.8    | 30.28        | 5.79          |
| microrouter              | 3.1.3   | ✓      | 31491.2    | 31.25        | 5.62          |
| trpc-router              | 9.27.4  | ✓      | 26846.8    | 36.74        | 5.94          |
| egg.js                   | 3.34.0  | ✓      | 16748.8    | 59.19        | 5.99          |
| express                  | 4.22.2  | ✓      | 13191.4    | 75.26        | 2.35          |
| express-with-middlewares | 4.22.2  | ✓      | 12783.6    | 77.69        | 4.75          |
| fastify-big-json         | 4.29.1  | ✓      | 12632.4    | 78.62        | 145.34        |
| express-route-prefix     | 4.22.2  | ✓      | 10406.6    | 95.50        | 3.85          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

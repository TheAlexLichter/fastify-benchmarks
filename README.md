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
* __Run:__ Mon Oct 28 2024 02:42:54 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 66016.4    | 14.65        | 11.77         |
| h3                       | 0.8.6   | ✗      | 66002.8    | 14.64        | 10.83         |
| 0http                    | 3.5.3   | ✓      | 65624.8    | 14.74        | 11.70         |
| h3-router                | 0.8.6   | ✓      | 63487.6    | 15.25        | 10.41         |
| bare                     | 10.13.0 | ✗      | 61181.6    | 15.86        | 10.91         |
| restana                  | 4.9.9   | ✓      | 60927.2    | 15.93        | 10.87         |
| polka                    | 0.5.2   | ✓      | 59708.8    | 16.25        | 10.65         |
| foxify                   | 0.10.20 | ✓      | 59257.6    | 16.37        | 9.72          |
| connect                  | 3.7.0   | ✗      | 57817.6    | 16.81        | 10.31         |
| fastify                  | 4.28.1  | ✓      | 57195.2    | 16.99        | 10.26         |
| micro                    | 9.4.1   | ✗      | 56848.8    | 17.10        | 10.14         |
| server-base              | 7.1.32  | ✗      | 55704.0    | 17.45        | 9.93          |
| server-base-router       | 7.1.32  | ✓      | 53701.6    | 18.12        | 9.58          |
| yeps                     | 1.1.1   | ✗      | 52333.6    | 18.61        | 9.33          |
| micro-route              | 2.5.0   | ✓      | 50504.0    | 19.30        | 9.01          |
| connect-router           | 1.3.8   | ✓      | 50322.4    | 19.37        | 8.97          |
| trek-engine              | 1.0.5   | ✗      | 47727.2    | 20.46        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 46484.0    | 21.01        | 7.63          |
| vapr                     | 0.6.0   | ✓      | 45935.2    | 21.27        | 7.53          |
| yeps-router              | 1.2.0   | ✓      | 44144.0    | 22.16        | 7.87          |
| spirit                   | 0.6.1   | ✗      | 43584.8    | 22.44        | 7.77          |
| spirit-router            | 0.5.0   | ✓      | 42904.8    | 22.79        | 7.65          |
| koa                      | 2.15.3  | ✗      | 42870.4    | 22.83        | 7.65          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40497.6    | 24.19        | 7.22          |
| restify                  | 8.6.1   | ✓      | 39416.2    | 24.87        | 7.10          |
| total.js                 | 3.4.13  | ✓      | 39408.2    | 24.88        | 12.06         |
| take-five                | 2.0.0   | ✓      | 38905.4    | 25.21        | 13.99         |
| koa-router               | 12.0.1  | ✓      | 38021.0    | 25.80        | 6.78          |
| hapi                     | 20.3.0  | ✓      | 34214.8    | 28.72        | 6.10          |
| microrouter              | 3.1.3   | ✓      | 32672.0    | 30.10        | 5.83          |
| trpc-router              | 9.27.4  | ✓      | 26845.2    | 36.75        | 5.94          |
| egg.js                   | 3.28.0  | ✓      | 17355.4    | 57.08        | 6.21          |
| express                  | 4.21.1  | ✓      | 13658.2    | 72.68        | 2.44          |
| fastify-big-json         | 4.28.1  | ✓      | 12890.0    | 77.05        | 148.30        |
| express-with-middlewares | 4.21.1  | ✓      | 12657.0    | 78.45        | 4.71          |
| express-route-prefix     | 4.21.1  | ✓      | 11103.2    | 89.51        | 4.11          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

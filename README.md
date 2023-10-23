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
* __Run:__ Mon Oct 23 2023 02:08:09 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| micro                    | 9.4.1   | ✗      | 31146.0    | 31.68        | 5.55          |
| polkadot                 | 1.0.0   | ✗      | 30190.4    | 32.74        | 5.38          |
| bare                     | 10.13.0 | ✗      | 29152.8    | 33.83        | 5.20          |
| polka                    | 0.5.2   | ✓      | 28809.2    | 34.25        | 5.14          |
| h3                       | 0.8.6   | ✗      | 28800.8    | 34.33        | 4.72          |
| h3-router                | 0.8.6   | ✓      | 28285.6    | 34.87        | 4.64          |
| fastify                  | 4.24.3  | ✓      | 28274.8    | 34.90        | 5.07          |
| foxify                   | 0.10.20 | ✓      | 27685.2    | 35.64        | 4.54          |
| 0http                    | 3.5.2   | ✓      | 27252.8    | 36.22        | 4.86          |
| server-base              | 7.1.32  | ✗      | 27010.4    | 36.55        | 4.82          |
| connect                  | 3.7.0   | ✗      | 26160.8    | 37.77        | 4.67          |
| trek-engine              | 1.0.5   | ✗      | 25393.9    | 38.90        | 4.17          |
| spirit-router            | 0.5.0   | ✓      | 25305.6    | 39.15        | 4.51          |
| restana                  | 4.9.7   | ✓      | 25246.4    | 39.12        | 4.50          |
| trek-router              | 1.2.0   | ✓      | 25186.3    | 39.22        | 4.13          |
| micro-route              | 2.5.0   | ✓      | 24955.6    | 39.59        | 4.45          |
| connect-router           | 1.3.8   | ✓      | 24914.4    | 39.63        | 4.44          |
| server-base-router       | 7.1.32  | ✓      | 24756.0    | 39.90        | 4.42          |
| yeps                     | 1.1.1   | ✗      | 24727.6    | 39.96        | 4.41          |
| spirit                   | 0.6.1   | ✗      | 24552.8    | 40.30        | 4.38          |
| yeps-router              | 1.2.0   | ✓      | 24418.8    | 40.44        | 4.36          |
| vapr                     | 0.6.0   | ✓      | 22045.1    | 44.86        | 3.62          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 21388.9    | 46.25        | 3.81          |
| restify                  | 8.6.1   | ✓      | 21318.8    | 46.39        | 3.84          |
| koa                      | 2.14.2  | ✗      | 21128.1    | 46.83        | 3.77          |
| take-five                | 2.0.0   | ✓      | 20190.9    | 49.02        | 7.26          |
| koa-router               | 12.0.1  | ✓      | 19375.9    | 51.10        | 3.46          |
| total.js                 | 3.4.13  | ✓      | 19002.3    | 52.12        | 5.82          |
| hapi                     | 20.3.0  | ✓      | 18512.3    | 53.51        | 3.30          |
| trpc-router              | 9.27.3  | ✓      | 16537.4    | 59.96        | 3.66          |
| microrouter              | 3.1.3   | ✓      | 16336.3    | 60.70        | 2.91          |
| egg.js                   | 3.17.5  | ✓      | 8882.4     | 111.97       | 3.18          |
| express                  | 4.18.2  | ✓      | 7064.9     | 140.84       | 1.26          |
| fastify-big-json         | 4.24.3  | ✓      | 6933.0     | 143.81       | 79.77         |
| express-with-middlewares | 4.18.2  | ✓      | 6256.6     | 159.11       | 2.33          |
| express-route-prefix     | 4.18.2  | ✓      | 5541.3     | 179.72       | 2.05          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

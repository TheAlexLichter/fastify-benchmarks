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
* __Run:__ Mon Feb 02 2026 03:43:31 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 82729.6    | 11.59        | 14.75         |
| polkadot                 | 1.0.0   | ✗      | 78321.6    | 12.26        | 13.97         |
| bare                     | 10.13.0 | ✗      | 76250.8    | 12.62        | 13.60         |
| foxify                   | 0.10.20 | ✓      | 76190.4    | 12.63        | 12.50         |
| h3                       | 0.8.6   | ✗      | 75361.6    | 12.77        | 12.36         |
| polka                    | 0.5.2   | ✓      | 72657.2    | 13.27        | 12.96         |
| h3-router                | 0.8.6   | ✓      | 72538.8    | 13.29        | 11.90         |
| connect                  | 3.7.0   | ✗      | 72029.2    | 13.39        | 12.85         |
| restana                  | 4.9.9   | ✓      | 71450.0    | 13.51        | 12.74         |
| micro                    | 9.4.1   | ✗      | 70526.0    | 13.68        | 12.58         |
| fastify                  | 4.29.1  | ✓      | 70414.0    | 13.71        | 12.62         |
| yeps                     | 1.1.1   | ✗      | 67501.2    | 14.32        | 12.04         |
| server-base              | 7.1.32  | ✗      | 66986.8    | 14.43        | 11.95         |
| connect-router           | 1.3.8   | ✓      | 66650.4    | 14.51        | 11.89         |
| server-base-router       | 7.1.32  | ✓      | 66369.2    | 14.57        | 11.84         |
| micro-route              | 2.5.0   | ✓      | 63662.8    | 15.21        | 11.35         |
| trek-router              | 1.2.0   | ✓      | 59168.8    | 16.40        | 9.71          |
| trek-engine              | 1.0.5   | ✗      | 59051.2    | 16.44        | 9.69          |
| vapr                     | 0.6.0   | ✓      | 59036.8    | 16.44        | 9.68          |
| yeps-router              | 1.2.0   | ✓      | 56666.4    | 17.15        | 10.11         |
| koa                      | 2.16.3  | ✗      | 53644.8    | 18.14        | 9.57          |
| take-five                | 2.0.0   | ✓      | 50291.2    | 19.38        | 18.08         |
| spirit                   | 0.6.1   | ✗      | 49999.2    | 19.50        | 8.92          |
| spirit-router            | 0.5.0   | ✓      | 49628.8    | 19.64        | 8.85          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 49174.4    | 19.84        | 8.77          |
| total.js                 | 3.4.13  | ✓      | 48661.6    | 20.05        | 14.90         |
| restify                  | 8.6.1   | ✓      | 46778.4    | 20.88        | 8.43          |
| koa-router               | 12.0.1  | ✓      | 45877.6    | 21.30        | 8.18          |
| hapi                     | 20.3.0  | ✓      | 40951.8    | 23.92        | 7.30          |
| microrouter              | 3.1.3   | ✓      | 39420.8    | 24.87        | 7.03          |
| trpc-router              | 9.27.4  | ✓      | 31974.8    | 30.77        | 7.07          |
| egg.js                   | 3.34.0  | ✓      | 20087.2    | 49.26        | 7.18          |
| express                  | 4.22.1  | ✓      | 16051.7    | 61.76        | 2.86          |
| express-with-middlewares | 4.22.1  | ✓      | 15209.8    | 65.20        | 5.66          |
| fastify-big-json         | 4.29.1  | ✓      | 13509.2    | 73.47        | 155.43        |
| express-route-prefix     | 4.22.1  | ✓      | 12506.8    | 79.40        | 4.63          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

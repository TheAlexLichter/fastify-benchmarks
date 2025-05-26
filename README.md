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
* __Run:__ Mon May 26 2025 02:58:57 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69828.8    | 13.82        | 12.45         |
| polkadot                 | 1.0.0   | ✗      | 68813.2    | 14.03        | 12.27         |
| h3                       | 0.8.6   | ✗      | 65345.2    | 14.81        | 10.72         |
| h3-router                | 0.8.6   | ✓      | 64270.4    | 15.06        | 10.54         |
| restana                  | 4.9.9   | ✓      | 62118.4    | 15.59        | 11.08         |
| bare                     | 10.13.0 | ✗      | 61867.2    | 15.66        | 11.03         |
| foxify                   | 0.10.20 | ✓      | 60471.2    | 16.05        | 9.92          |
| connect                  | 3.7.0   | ✗      | 59010.4    | 16.45        | 10.52         |
| polka                    | 0.5.2   | ✓      | 58627.2    | 16.56        | 10.46         |
| fastify                  | 4.29.1  | ✓      | 58093.6    | 16.71        | 10.42         |
| server-base              | 7.1.32  | ✗      | 56496.8    | 17.20        | 10.07         |
| server-base-router       | 7.1.32  | ✓      | 56374.4    | 17.25        | 10.05         |
| micro                    | 9.4.1   | ✗      | 56332.8    | 17.25        | 10.05         |
| yeps                     | 1.1.1   | ✗      | 53292.8    | 18.26        | 9.50          |
| connect-router           | 1.3.8   | ✓      | 51497.6    | 18.91        | 9.18          |
| micro-route              | 2.5.0   | ✓      | 51216.8    | 19.03        | 9.13          |
| trek-engine              | 1.0.5   | ✗      | 48752.0    | 20.01        | 8.00          |
| trek-router              | 1.2.0   | ✓      | 47975.2    | 20.35        | 7.87          |
| vapr                     | 0.6.0   | ✓      | 45853.6    | 21.31        | 7.52          |
| spirit                   | 0.6.1   | ✗      | 44543.2    | 21.96        | 7.94          |
| yeps-router              | 1.2.0   | ✓      | 43592.8    | 22.44        | 7.77          |
| koa                      | 2.16.1  | ✗      | 43066.4    | 22.71        | 7.68          |
| spirit-router            | 0.5.0   | ✓      | 42821.6    | 22.85        | 7.64          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40240.6    | 24.35        | 7.18          |
| restify                  | 8.6.1   | ✓      | 39385.0    | 24.88        | 7.10          |
| total.js                 | 3.4.13  | ✓      | 39338.4    | 24.93        | 12.04         |
| take-five                | 2.0.0   | ✓      | 38387.8    | 25.55        | 13.80         |
| koa-router               | 12.0.1  | ✓      | 36921.8    | 26.57        | 6.58          |
| hapi                     | 20.3.0  | ✓      | 33928.0    | 28.98        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 31992.6    | 30.75        | 5.71          |
| trpc-router              | 9.27.4  | ✓      | 26846.8    | 36.74        | 5.94          |
| egg.js                   | 3.30.1  | ✓      | 17245.9    | 57.47        | 6.17          |
| express                  | 4.21.2  | ✓      | 13660.8    | 72.65        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12915.4    | 76.88        | 148.61        |
| express-with-middlewares | 4.21.2  | ✓      | 12352.4    | 80.41        | 4.59          |
| express-route-prefix     | 4.21.2  | ✓      | 10955.8    | 90.69        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

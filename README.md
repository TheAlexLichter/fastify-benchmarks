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
* __Run:__ Mon Dec 29 2025 03:18:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69930.0    | 13.79        | 12.47         |
| 0http                    | 3.5.3   | ✓      | 69382.0    | 13.91        | 12.37         |
| h3                       | 0.8.6   | ✗      | 66978.0    | 14.42        | 10.99         |
| h3-router                | 0.8.6   | ✓      | 66571.2    | 14.51        | 10.92         |
| restana                  | 4.9.9   | ✓      | 62564.8    | 15.47        | 11.16         |
| bare                     | 10.13.0 | ✗      | 61244.8    | 15.84        | 10.92         |
| foxify                   | 0.10.20 | ✓      | 59563.2    | 16.29        | 9.77          |
| polka                    | 0.5.2   | ✓      | 57825.6    | 16.79        | 10.31         |
| micro                    | 9.4.1   | ✗      | 57079.2    | 17.03        | 10.18         |
| server-base-router       | 7.1.32  | ✓      | 57005.6    | 17.06        | 10.17         |
| server-base              | 7.1.32  | ✗      | 56833.6    | 17.11        | 10.14         |
| connect                  | 3.7.0   | ✗      | 56709.6    | 17.13        | 10.11         |
| fastify                  | 4.29.1  | ✓      | 56567.2    | 17.19        | 10.14         |
| yeps                     | 1.1.1   | ✗      | 54226.4    | 17.94        | 9.67          |
| connect-router           | 1.3.8   | ✓      | 52337.6    | 18.61        | 9.33          |
| micro-route              | 2.5.0   | ✓      | 50570.4    | 19.28        | 9.02          |
| trek-engine              | 1.0.5   | ✗      | 48975.2    | 19.92        | 8.03          |
| trek-router              | 1.2.0   | ✓      | 48474.4    | 20.14        | 7.95          |
| vapr                     | 0.6.0   | ✓      | 46220.8    | 21.13        | 7.58          |
| spirit                   | 0.6.1   | ✗      | 44371.2    | 22.08        | 7.91          |
| yeps-router              | 1.2.0   | ✓      | 44144.8    | 22.15        | 7.87          |
| spirit-router            | 0.5.0   | ✓      | 43800.8    | 22.31        | 7.81          |
| koa                      | 2.16.3  | ✗      | 42264.8    | 23.17        | 7.54          |
| total.js                 | 3.4.13  | ✓      | 40095.2    | 24.44        | 12.28         |
| take-five                | 2.0.0   | ✓      | 39060.6    | 25.10        | 14.04         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39024.0    | 25.13        | 6.96          |
| restify                  | 8.6.1   | ✓      | 38836.2    | 25.26        | 7.00          |
| koa-router               | 12.0.1  | ✓      | 36856.2    | 26.63        | 6.57          |
| hapi                     | 20.3.0  | ✓      | 33623.0    | 29.25        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 31680.4    | 31.07        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 27156.4    | 36.32        | 6.01          |
| egg.js                   | 3.32.0  | ✓      | 17362.9    | 57.06        | 6.21          |
| express                  | 4.22.1  | ✓      | 13436.4    | 73.87        | 2.40          |
| fastify-big-json         | 4.29.1  | ✓      | 12713.2    | 78.13        | 146.27        |
| express-with-middlewares | 4.22.1  | ✓      | 12234.0    | 81.19        | 4.55          |
| express-route-prefix     | 4.22.1  | ✓      | 10718.9    | 92.73        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

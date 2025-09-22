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
* __Run:__ Mon Sep 22 2025 02:54:13 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 71198.0    | 13.55        | 12.70         |
| polkadot                 | 1.0.0   | ✗      | 68579.6    | 14.08        | 12.23         |
| h3                       | 0.8.6   | ✗      | 65921.6    | 14.67        | 10.81         |
| h3-router                | 0.8.6   | ✓      | 63474.4    | 15.25        | 10.41         |
| restana                  | 4.9.9   | ✓      | 62478.4    | 15.50        | 11.14         |
| bare                     | 10.13.0 | ✗      | 62151.2    | 15.58        | 11.08         |
| foxify                   | 0.10.20 | ✓      | 59237.6    | 16.39        | 9.72          |
| polka                    | 0.5.2   | ✓      | 59062.4    | 16.44        | 10.53         |
| connect                  | 3.7.0   | ✗      | 58639.2    | 16.55        | 10.46         |
| fastify                  | 4.29.1  | ✓      | 57872.8    | 16.79        | 10.38         |
| micro                    | 9.4.1   | ✗      | 57729.6    | 16.83        | 10.29         |
| server-base-router       | 7.1.32  | ✓      | 56316.8    | 17.26        | 10.04         |
| server-base              | 7.1.32  | ✗      | 55855.2    | 17.41        | 9.96          |
| yeps                     | 1.1.1   | ✗      | 53310.4    | 18.27        | 9.51          |
| connect-router           | 1.3.8   | ✓      | 51039.2    | 19.09        | 9.10          |
| micro-route              | 2.5.0   | ✓      | 50764.8    | 19.19        | 9.05          |
| trek-engine              | 1.0.5   | ✗      | 49446.4    | 19.72        | 8.11          |
| trek-router              | 1.2.0   | ✓      | 47738.4    | 20.45        | 7.83          |
| vapr                     | 0.6.0   | ✓      | 46997.6    | 20.78        | 7.71          |
| yeps-router              | 1.2.0   | ✓      | 44340.8    | 22.05        | 7.91          |
| spirit                   | 0.6.1   | ✗      | 43298.4    | 22.62        | 7.72          |
| koa                      | 2.16.2  | ✗      | 42738.4    | 22.91        | 7.62          |
| spirit-router            | 0.5.0   | ✓      | 42310.4    | 23.15        | 7.55          |
| total.js                 | 3.4.13  | ✓      | 40840.8    | 23.99        | 12.50         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40203.0    | 24.37        | 7.17          |
| restify                  | 8.6.1   | ✓      | 39987.2    | 24.51        | 7.21          |
| take-five                | 2.0.0   | ✓      | 39215.4    | 25.00        | 14.10         |
| koa-router               | 12.0.1  | ✓      | 37215.8    | 26.38        | 6.64          |
| hapi                     | 20.3.0  | ✓      | 34346.8    | 28.60        | 6.13          |
| microrouter              | 3.1.3   | ✓      | 32161.0    | 30.60        | 5.74          |
| trpc-router              | 9.27.4  | ✓      | 27710.0    | 35.58        | 6.13          |
| egg.js                   | 3.31.0  | ✓      | 17462.3    | 56.71        | 6.24          |
| express                  | 4.21.2  | ✓      | 13467.2    | 73.71        | 2.40          |
| fastify-big-json         | 4.29.1  | ✓      | 12747.6    | 77.88        | 146.68        |
| express-with-middlewares | 4.21.2  | ✓      | 12647.4    | 78.50        | 4.70          |
| express-route-prefix     | 4.21.2  | ✓      | 10883.6    | 91.30        | 4.03          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

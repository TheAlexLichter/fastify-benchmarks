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
* __Run:__ Mon May 11 2026 05:03:41 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 74871.6    | 12.86        | 13.35         |
| polkadot                 | 1.0.0   | ✗      | 74444.8    | 12.93        | 13.28         |
| bare                     | 10.13.0 | ✗      | 72926.0    | 13.21        | 13.01         |
| polka                    | 0.5.2   | ✓      | 71189.2    | 13.55        | 12.70         |
| h3-router                | 0.8.6   | ✓      | 70503.6    | 13.68        | 11.57         |
| h3                       | 0.8.6   | ✗      | 70179.6    | 13.75        | 11.51         |
| foxify                   | 0.10.20 | ✓      | 69787.6    | 13.84        | 11.45         |
| connect                  | 3.7.0   | ✗      | 69566.8    | 13.88        | 12.41         |
| server-base-router       | 7.1.32  | ✓      | 68524.4    | 14.10        | 12.22         |
| server-base              | 7.1.32  | ✗      | 68386.0    | 14.13        | 12.19         |
| restana                  | 4.9.9   | ✓      | 67950.0    | 14.23        | 12.12         |
| micro                    | 9.4.1   | ✗      | 67106.0    | 14.40        | 11.97         |
| yeps                     | 1.1.1   | ✗      | 66082.8    | 14.63        | 11.79         |
| fastify                  | 4.29.1  | ✓      | 65953.6    | 14.66        | 11.82         |
| connect-router           | 1.3.8   | ✓      | 63741.6    | 15.19        | 11.37         |
| micro-route              | 2.5.0   | ✓      | 61137.6    | 15.86        | 10.90         |
| vapr                     | 0.6.0   | ✓      | 58145.6    | 16.71        | 9.54          |
| trek-engine              | 1.0.5   | ✗      | 55672.0    | 17.46        | 9.13          |
| trek-router              | 1.2.0   | ✓      | 54503.2    | 17.85        | 8.94          |
| yeps-router              | 1.2.0   | ✓      | 52794.4    | 18.44        | 9.42          |
| total.js                 | 3.4.13  | ✓      | 51738.4    | 18.83        | 15.84         |
| take-five                | 2.0.0   | ✓      | 51642.4    | 18.87        | 18.57         |
| koa                      | 2.16.4  | ✗      | 50520.0    | 19.29        | 9.01          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 46881.6    | 20.83        | 8.36          |
| restify                  | 8.6.1   | ✓      | 45664.0    | 21.40        | 8.23          |
| spirit                   | 0.6.1   | ✗      | 45142.4    | 21.70        | 8.05          |
| koa-router               | 12.0.1  | ✓      | 44475.2    | 21.98        | 7.93          |
| spirit-router            | 0.5.0   | ✓      | 42956.8    | 22.76        | 7.66          |
| microrouter              | 3.1.3   | ✓      | 41074.2    | 23.85        | 7.32          |
| hapi                     | 20.3.0  | ✓      | 37925.4    | 25.86        | 6.76          |
| trpc-router              | 9.27.4  | ✓      | 31457.6    | 31.29        | 6.96          |
| egg.js                   | 3.34.0  | ✓      | 19205.9    | 51.54        | 6.87          |
| express                  | 4.22.1  | ✓      | 15886.6    | 62.40        | 2.83          |
| express-with-middlewares | 4.22.1  | ✓      | 15142.4    | 65.50        | 5.63          |
| fastify-big-json         | 4.29.1  | ✓      | 12777.2    | 77.72        | 147.01        |
| express-route-prefix     | 4.22.1  | ✓      | 12166.8    | 81.63        | 4.50          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

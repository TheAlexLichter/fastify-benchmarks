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
* __Run:__ Mon Oct 27 2025 03:00:00 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 67236.0    | 14.39        | 11.99         |
| h3-router                | 0.8.6   | ✓      | 65645.2    | 14.73        | 10.77         |
| h3                       | 0.8.6   | ✗      | 65454.4    | 14.78        | 10.74         |
| polkadot                 | 1.0.0   | ✗      | 65011.2    | 14.87        | 11.59         |
| restana                  | 4.9.9   | ✓      | 61170.4    | 15.86        | 10.91         |
| bare                     | 10.13.0 | ✗      | 60508.8    | 16.04        | 10.79         |
| foxify                   | 0.10.20 | ✓      | 59357.6    | 16.35        | 9.74          |
| fastify                  | 4.29.1  | ✓      | 58268.0    | 16.67        | 10.45         |
| polka                    | 0.5.2   | ✓      | 58142.4    | 16.71        | 10.37         |
| connect                  | 3.7.0   | ✗      | 56688.8    | 17.13        | 10.11         |
| micro                    | 9.4.1   | ✗      | 56249.6    | 17.28        | 10.03         |
| server-base-router       | 7.1.32  | ✓      | 55871.2    | 17.41        | 9.96          |
| server-base              | 7.1.32  | ✗      | 55312.0    | 17.59        | 9.86          |
| yeps                     | 1.1.1   | ✗      | 52916.0    | 18.40        | 9.44          |
| micro-route              | 2.5.0   | ✓      | 50640.0    | 19.24        | 9.03          |
| connect-router           | 1.3.8   | ✓      | 50272.8    | 19.39        | 8.97          |
| trek-engine              | 1.0.5   | ✗      | 47913.6    | 20.38        | 7.86          |
| trek-router              | 1.2.0   | ✓      | 46654.4    | 20.94        | 7.65          |
| vapr                     | 0.6.0   | ✓      | 45685.6    | 21.39        | 7.49          |
| yeps-router              | 1.2.0   | ✓      | 43904.0    | 22.28        | 7.83          |
| spirit-router            | 0.5.0   | ✓      | 41837.6    | 23.41        | 7.46          |
| koa                      | 2.16.3  | ✗      | 41300.8    | 23.71        | 7.37          |
| spirit                   | 0.6.1   | ✗      | 41045.6    | 23.88        | 7.32          |
| total.js                 | 3.4.13  | ✓      | 39976.0    | 24.51        | 12.24         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39687.4    | 24.70        | 7.08          |
| restify                  | 8.6.1   | ✓      | 39364.2    | 24.90        | 7.10          |
| take-five                | 2.0.0   | ✓      | 39096.6    | 25.07        | 14.06         |
| koa-router               | 12.0.1  | ✓      | 36185.8    | 27.14        | 6.45          |
| hapi                     | 20.3.0  | ✓      | 33507.8    | 29.34        | 5.98          |
| microrouter              | 3.1.3   | ✓      | 31642.6    | 31.10        | 5.64          |
| trpc-router              | 9.27.4  | ✓      | 27156.0    | 36.32        | 6.01          |
| egg.js                   | 3.31.0  | ✓      | 17490.7    | 56.65        | 6.25          |
| express                  | 4.21.2  | ✓      | 13398.0    | 74.10        | 2.39          |
| fastify-big-json         | 4.29.1  | ✓      | 12890.6    | 77.04        | 148.32        |
| express-with-middlewares | 4.21.2  | ✓      | 12536.4    | 79.21        | 4.66          |
| express-route-prefix     | 4.21.2  | ✓      | 11025.0    | 90.12        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

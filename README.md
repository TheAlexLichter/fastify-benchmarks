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
* __Run:__ Mon Apr 22 2024 02:11:21 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68729.6    | 14.06        | 12.26         |
| polkadot                 | 1.0.0   | ✗      | 66656.4    | 14.51        | 11.89         |
| h3-router                | 0.8.6   | ✓      | 63500.8    | 15.24        | 10.42         |
| h3                       | 0.8.6   | ✗      | 61845.6    | 15.67        | 10.14         |
| restana                  | 4.9.9   | ✓      | 61439.2    | 15.78        | 10.96         |
| bare                     | 10.13.0 | ✗      | 60984.8    | 15.90        | 10.88         |
| foxify                   | 0.10.20 | ✓      | 59439.2    | 16.32        | 9.75          |
| connect                  | 3.7.0   | ✗      | 57057.6    | 17.02        | 10.18         |
| fastify                  | 4.26.2  | ✓      | 56688.0    | 17.14        | 10.16         |
| micro                    | 9.4.1   | ✗      | 55868.0    | 17.40        | 9.96          |
| polka                    | 0.5.2   | ✓      | 55738.4    | 17.44        | 9.94          |
| server-base-router       | 7.1.32  | ✓      | 54006.4    | 18.02        | 9.63          |
| server-base              | 7.1.32  | ✗      | 53524.8    | 18.18        | 9.55          |
| connect-router           | 1.3.8   | ✓      | 50975.2    | 19.13        | 9.09          |
| micro-route              | 2.5.0   | ✓      | 49603.2    | 19.66        | 8.85          |
| yeps                     | 1.1.1   | ✗      | 48240.0    | 20.23        | 8.60          |
| trek-router              | 1.2.0   | ✓      | 46220.8    | 21.14        | 7.58          |
| trek-engine              | 1.0.5   | ✗      | 45901.6    | 21.29        | 7.53          |
| vapr                     | 0.6.0   | ✓      | 44184.8    | 22.13        | 7.25          |
| spirit-router            | 0.5.0   | ✓      | 44118.4    | 22.20        | 7.87          |
| spirit                   | 0.6.1   | ✗      | 44064.8    | 22.21        | 7.86          |
| yeps-router              | 1.2.0   | ✓      | 42945.6    | 22.78        | 7.66          |
| koa                      | 2.15.3  | ✗      | 42503.2    | 23.03        | 7.58          |
| total.js                 | 3.4.13  | ✓      | 40390.4    | 24.26        | 12.36         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40231.4    | 24.35        | 7.17          |
| restify                  | 8.6.1   | ✓      | 39798.2    | 24.62        | 7.17          |
| take-five                | 2.0.0   | ✓      | 39243.4    | 24.98        | 14.11         |
| koa-router               | 12.0.1  | ✓      | 36767.4    | 26.70        | 6.56          |
| hapi                     | 20.3.0  | ✓      | 34151.2    | 28.77        | 6.09          |
| microrouter              | 3.1.3   | ✓      | 31680.6    | 31.06        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 26634.0    | 37.04        | 5.89          |
| egg.js                   | 3.22.0  | ✓      | 17596.5    | 56.31        | 6.29          |
| express                  | 4.19.2  | ✓      | 14202.4    | 69.87        | 2.53          |
| fastify-big-json         | 4.26.2  | ✓      | 13052.2    | 76.06        | 150.18        |
| express-with-middlewares | 4.19.2  | ✓      | 12464.2    | 79.68        | 4.64          |
| express-route-prefix     | 4.19.2  | ✓      | 11031.8    | 90.05        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

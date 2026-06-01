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
* __Run:__ Mon Jun 01 2026 05:55:29 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 64458.4    | 15.02        | 11.49         |
| polkadot                 | 1.0.0   | ✗      | 60947.2    | 15.91        | 10.87         |
| bare                     | 10.13.0 | ✗      | 58578.4    | 16.57        | 10.45         |
| h3                       | 0.8.6   | ✗      | 58317.6    | 16.64        | 9.57          |
| polka                    | 0.5.2   | ✓      | 56495.2    | 17.20        | 10.07         |
| foxify                   | 0.10.20 | ✓      | 56200.8    | 17.30        | 9.22          |
| h3-router                | 0.8.6   | ✓      | 55849.6    | 17.41        | 9.16          |
| restana                  | 4.9.9   | ✓      | 55060.0    | 17.67        | 9.82          |
| connect                  | 3.7.0   | ✗      | 54327.2    | 17.91        | 9.69          |
| micro                    | 9.4.1   | ✗      | 54024.0    | 18.01        | 9.63          |
| fastify                  | 4.29.1  | ✓      | 53588.8    | 18.16        | 9.61          |
| server-base              | 7.1.32  | ✗      | 51874.4    | 18.78        | 9.25          |
| server-base-router       | 7.1.32  | ✓      | 51225.6    | 19.03        | 9.14          |
| micro-route              | 2.5.0   | ✓      | 49333.6    | 19.77        | 8.80          |
| connect-router           | 1.3.8   | ✓      | 49153.6    | 19.85        | 8.77          |
| yeps                     | 1.1.1   | ✗      | 47921.6    | 20.37        | 8.55          |
| trek-engine              | 1.0.5   | ✗      | 44944.8    | 21.75        | 7.37          |
| trek-router              | 1.2.0   | ✓      | 44152.6    | 22.15        | 7.24          |
| vapr                     | 0.6.0   | ✓      | 43604.8    | 22.43        | 7.15          |
| yeps-router              | 1.2.0   | ✓      | 40814.2    | 24.01        | 7.28          |
| koa                      | 2.16.4  | ✗      | 40660.8    | 24.10        | 7.25          |
| spirit                   | 0.6.1   | ✗      | 38955.2    | 25.18        | 6.95          |
| total.js                 | 3.4.13  | ✓      | 38072.6    | 25.77        | 11.66         |
| spirit-router            | 0.5.0   | ✓      | 38011.2    | 25.81        | 6.78          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37077.0    | 26.47        | 6.61          |
| take-five                | 2.0.0   | ✓      | 37060.6    | 26.48        | 13.32         |
| restify                  | 8.6.1   | ✓      | 36265.8    | 27.08        | 6.54          |
| koa-router               | 12.0.1  | ✓      | 35067.8    | 28.01        | 6.25          |
| hapi                     | 20.3.0  | ✓      | 31611.2    | 31.13        | 5.64          |
| microrouter              | 3.1.3   | ✓      | 31034.4    | 31.71        | 5.53          |
| trpc-router              | 9.27.4  | ✓      | 24919.6    | 39.62        | 5.51          |
| egg.js                   | 3.34.0  | ✓      | 16914.1    | 58.61        | 6.05          |
| express                  | 4.22.2  | ✓      | 12882.0    | 77.08        | 2.30          |
| fastify-big-json         | 4.29.1  | ✓      | 12092.6    | 82.12        | 139.14        |
| express-with-middlewares | 4.22.2  | ✓      | 12061.6    | 82.35        | 4.49          |
| express-route-prefix     | 4.22.2  | ✓      | 10019.4    | 99.20        | 3.71          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Feb 05 2024 02:08:46 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68016.4    | 14.21        | 12.13         |
| 0http                    | 3.5.2   | ✓      | 65344.4    | 14.80        | 11.65         |
| h3-router                | 0.8.6   | ✓      | 64616.4    | 14.99        | 10.60         |
| h3                       | 0.8.6   | ✗      | 63712.8    | 15.21        | 10.45         |
| bare                     | 10.13.0 | ✗      | 59899.2    | 16.18        | 10.68         |
| restana                  | 4.9.7   | ✓      | 57933.6    | 16.76        | 10.33         |
| foxify                   | 0.10.20 | ✓      | 57352.0    | 16.94        | 9.41          |
| polka                    | 0.5.2   | ✓      | 57074.4    | 17.03        | 10.18         |
| connect                  | 3.7.0   | ✗      | 56826.4    | 17.10        | 10.13         |
| micro                    | 9.4.1   | ✗      | 56208.0    | 17.29        | 10.02         |
| server-base-router       | 7.1.32  | ✓      | 53445.6    | 18.21        | 9.53          |
| fastify                  | 4.26.0  | ✓      | 53283.2    | 18.27        | 9.55          |
| server-base              | 7.1.32  | ✗      | 53135.2    | 18.32        | 9.48          |
| yeps                     | 1.1.1   | ✗      | 51854.4    | 18.79        | 9.25          |
| connect-router           | 1.3.8   | ✓      | 49938.4    | 19.52        | 8.91          |
| micro-route              | 2.5.0   | ✓      | 49402.4    | 19.74        | 8.81          |
| trek-engine              | 1.0.5   | ✗      | 48216.0    | 20.24        | 7.91          |
| trek-router              | 1.2.0   | ✓      | 47284.0    | 20.65        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 44777.6    | 21.85        | 7.34          |
| spirit                   | 0.6.1   | ✗      | 44220.0    | 22.18        | 7.89          |
| spirit-router            | 0.5.0   | ✓      | 43241.6    | 22.61        | 7.71          |
| yeps-router              | 1.2.0   | ✓      | 43045.6    | 22.72        | 7.68          |
| koa                      | 2.15.0  | ✗      | 42977.6    | 22.78        | 7.66          |
| restify                  | 8.6.1   | ✓      | 39596.8    | 24.74        | 7.14          |
| total.js                 | 3.4.13  | ✓      | 39564.0    | 24.78        | 12.11         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39222.6    | 24.99        | 6.99          |
| take-five                | 2.0.0   | ✓      | 38894.2    | 25.21        | 13.98         |
| koa-router               | 12.0.1  | ✓      | 36926.6    | 26.58        | 6.59          |
| hapi                     | 20.3.0  | ✓      | 33654.2    | 29.22        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 32075.0    | 30.66        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 26983.2    | 36.55        | 5.97          |
| egg.js                   | 3.18.0  | ✓      | 17589.3    | 56.35        | 6.29          |
| express                  | 4.18.2  | ✓      | 13516.6    | 73.44        | 2.41          |
| fastify-big-json         | 4.26.0  | ✓      | 12977.2    | 76.52        | 149.32        |
| express-with-middlewares | 4.18.2  | ✓      | 12426.0    | 79.93        | 4.62          |
| express-route-prefix     | 4.18.2  | ✓      | 11026.2    | 90.10        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

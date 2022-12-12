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
* __Node:__ `v14.21.1`
* __Run:__ Mon Dec 12 2022 02:37:54 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 64295.2    | 15.05        | 11.47         |
| bare                     | 10.13.0 | ✗      | 61608.0    | 15.74        | 10.99         |
| h3-router                | 0.8.6   | ✓      | 60891.2    | 15.90        | 9.99          |
| 0http                    | 3.4.2   | ✓      | 60672.8    | 16.02        | 10.82         |
| h3                       | 0.8.6   | ✗      | 60571.2    | 15.99        | 9.93          |
| foxify                   | 0.10.20 | ✓      | 60191.2    | 16.12        | 9.87          |
| polka                    | 0.5.2   | ✓      | 60066.4    | 16.18        | 10.71         |
| fastify                  | 4.10.2  | ✓      | 59115.2    | 16.42        | 10.60         |
| micro                    | 9.4.1   | ✗      | 57564.0    | 16.88        | 10.27         |
| connect                  | 3.7.0   | ✗      | 57163.0    | 17.00        | 10.19         |
| server-base              | 7.1.32  | ✗      | 55909.6    | 17.38        | 9.97          |
| server-base-router       | 7.1.32  | ✓      | 55699.2    | 17.46        | 9.93          |
| restana                  | 4.9.7   | ✓      | 55362.4    | 17.47        | 9.87          |
| yeps                     | 1.1.1   | ✗      | 53536.0    | 18.18        | 9.55          |
| connect-router           | 1.3.7   | ✓      | 53140.8    | 18.33        | 9.48          |
| micro-route              | 2.5.0   | ✓      | 52549.6    | 18.52        | 9.37          |
| trek-engine              | 1.0.5   | ✗      | 50735.8    | 19.21        | 8.32          |
| trek-router              | 1.2.0   | ✓      | 49807.0    | 19.58        | 8.17          |
| vapr                     | 0.6.0   | ✓      | 48122.4    | 20.29        | 7.89          |
| yeps-router              | 1.2.0   | ✓      | 45842.4    | 21.32        | 8.18          |
| spirit-router            | 0.5.0   | ✓      | 45047.2    | 21.71        | 8.03          |
| spirit                   | 0.6.1   | ✗      | 44955.2    | 21.75        | 8.02          |
| koa                      | 2.14.1  | ✗      | 44849.6    | 21.80        | 8.00          |
| take-five                | 2.0.0   | ✓      | 41681.4    | 23.49        | 14.98         |
| total.js                 | 3.4.13  | ✓      | 41529.6    | 23.59        | 12.71         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41439.4    | 23.64        | 7.39          |
| restify                  | 8.6.1   | ✓      | 39448.2    | 24.85        | 7.11          |
| koa-router               | 12.0.0  | ✓      | 38616.8    | 25.40        | 6.89          |
| hapi                     | 20.2.2  | ✓      | 34116.4    | 28.81        | 6.08          |
| microrouter              | 3.1.3   | ✓      | 32804.6    | 29.98        | 5.85          |
| trpc-router              | 9.27.4  | ✓      | 28665.2    | 34.38        | 6.34          |
| egg.js                   | 3.8.0   | ✓      | 17574.4    | 56.35        | 6.28          |
| express                  | 4.18.2  | ✓      | 14000.4    | 70.88        | 2.50          |
| express-with-middlewares | 4.18.2  | ✓      | 12380.4    | 80.21        | 4.60          |
| express-route-prefix     | 4.18.2  | ✓      | 12107.6    | 82.05        | 4.48          |
| fastify-big-json         | 4.10.2  | ✓      | 11922.8    | 83.40        | 137.16        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

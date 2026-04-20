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
* __Run:__ Mon Apr 20 2026 04:33:27 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69519.6    | 13.90        | 12.40         |
| polkadot                 | 1.0.0   | ✗      | 67952.8    | 14.22        | 12.12         |
| h3                       | 0.8.6   | ✗      | 67897.6    | 14.24        | 11.14         |
| h3-router                | 0.8.6   | ✓      | 65889.2    | 14.67        | 10.81         |
| restana                  | 4.9.9   | ✓      | 61545.6    | 15.78        | 10.98         |
| bare                     | 10.13.0 | ✗      | 61385.6    | 15.80        | 10.95         |
| foxify                   | 0.10.20 | ✓      | 61104.0    | 15.87        | 10.02         |
| polka                    | 0.5.2   | ✓      | 59228.0    | 16.39        | 10.56         |
| connect                  | 3.7.0   | ✗      | 58588.8    | 16.57        | 10.45         |
| server-base-router       | 7.1.32  | ✓      | 57724.0    | 16.82        | 10.29         |
| server-base              | 7.1.32  | ✗      | 57356.0    | 16.94        | 10.23         |
| micro                    | 9.4.1   | ✗      | 56934.4    | 17.06        | 10.15         |
| fastify                  | 4.29.1  | ✓      | 56690.4    | 17.14        | 10.16         |
| yeps                     | 1.1.1   | ✗      | 52872.0    | 18.43        | 9.43          |
| connect-router           | 1.3.8   | ✓      | 51567.2    | 18.90        | 9.20          |
| micro-route              | 2.5.0   | ✓      | 51250.4    | 19.02        | 9.14          |
| trek-engine              | 1.0.5   | ✗      | 50067.2    | 19.48        | 8.21          |
| trek-router              | 1.2.0   | ✓      | 48598.4    | 20.08        | 7.97          |
| vapr                     | 0.6.0   | ✓      | 47192.0    | 20.69        | 7.74          |
| spirit                   | 0.6.1   | ✗      | 44467.2    | 21.99        | 7.93          |
| spirit-router            | 0.5.0   | ✓      | 43908.0    | 22.26        | 7.83          |
| yeps-router              | 1.2.0   | ✓      | 43447.2    | 22.52        | 7.75          |
| koa                      | 2.16.4  | ✗      | 43359.2    | 22.56        | 7.73          |
| total.js                 | 3.4.13  | ✓      | 40776.2    | 24.02        | 12.48         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39583.4    | 24.76        | 7.06          |
| take-five                | 2.0.0   | ✓      | 39552.6    | 24.79        | 14.22         |
| restify                  | 8.6.1   | ✓      | 38823.0    | 25.25        | 7.00          |
| koa-router               | 12.0.1  | ✓      | 36561.8    | 26.85        | 6.52          |
| hapi                     | 20.3.0  | ✓      | 33047.4    | 29.75        | 5.89          |
| microrouter              | 3.1.3   | ✓      | 32216.2    | 30.54        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 27619.2    | 35.70        | 6.11          |
| egg.js                   | 3.34.0  | ✓      | 17642.8    | 56.17        | 6.31          |
| express                  | 4.22.1  | ✓      | 13209.0    | 75.18        | 2.36          |
| express-with-middlewares | 4.22.1  | ✓      | 12613.2    | 78.74        | 4.69          |
| fastify-big-json         | 4.29.1  | ✓      | 12379.4    | 80.24        | 142.43        |
| express-route-prefix     | 4.22.1  | ✓      | 10422.5    | 95.38        | 3.86          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

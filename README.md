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
* __Run:__ Mon Apr 08 2024 02:09:09 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 70573.6    | 13.69        | 12.59         |
| polkadot                 | 1.0.0   | ✗      | 70162.0    | 13.75        | 12.51         |
| h3-router                | 0.8.6   | ✓      | 66172.0    | 14.61        | 10.85         |
| h3                       | 0.8.6   | ✗      | 65756.4    | 14.72        | 10.79         |
| restana                  | 4.9.9   | ✓      | 63723.6    | 15.21        | 11.36         |
| bare                     | 10.13.0 | ✗      | 61382.4    | 15.80        | 10.95         |
| connect                  | 3.7.0   | ✗      | 59936.0    | 16.18        | 10.69         |
| foxify                   | 0.10.20 | ✓      | 59671.2    | 16.26        | 9.79          |
| polka                    | 0.5.2   | ✓      | 58572.8    | 16.57        | 10.45         |
| fastify                  | 4.26.2  | ✓      | 57087.2    | 17.03        | 10.24         |
| micro                    | 9.4.1   | ✗      | 56755.2    | 17.12        | 10.12         |
| server-base-router       | 7.1.32  | ✓      | 56239.2    | 17.28        | 10.03         |
| server-base              | 7.1.32  | ✗      | 55281.6    | 17.60        | 9.86          |
| yeps                     | 1.1.1   | ✗      | 55217.6    | 17.62        | 9.85          |
| connect-router           | 1.3.8   | ✓      | 51397.6    | 18.97        | 9.17          |
| micro-route              | 2.5.0   | ✓      | 50888.0    | 19.15        | 9.08          |
| trek-engine              | 1.0.5   | ✗      | 49084.8    | 19.87        | 8.05          |
| trek-router              | 1.2.0   | ✓      | 48155.2    | 20.28        | 7.90          |
| vapr                     | 0.6.0   | ✓      | 47056.8    | 20.75        | 7.72          |
| spirit                   | 0.6.1   | ✗      | 45687.2    | 21.44        | 8.15          |
| yeps-router              | 1.2.0   | ✓      | 43935.2    | 22.25        | 7.84          |
| spirit-router            | 0.5.0   | ✓      | 43613.6    | 22.40        | 7.78          |
| koa                      | 2.15.2  | ✗      | 43198.4    | 22.66        | 7.70          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40597.0    | 24.12        | 7.24          |
| restify                  | 8.6.1   | ✓      | 40023.2    | 24.48        | 7.21          |
| take-five                | 2.0.0   | ✓      | 39171.0    | 25.02        | 14.08         |
| total.js                 | 3.4.13  | ✓      | 39092.8    | 25.07        | 11.97         |
| koa-router               | 12.0.1  | ✓      | 38497.4    | 25.46        | 6.87          |
| hapi                     | 20.3.0  | ✓      | 34070.8    | 28.83        | 6.08          |
| microrouter              | 3.1.3   | ✓      | 32065.8    | 30.67        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 26805.6    | 36.79        | 5.93          |
| egg.js                   | 3.21.0  | ✓      | 17801.3    | 55.66        | 6.37          |
| express                  | 4.19.2  | ✓      | 13715.0    | 72.38        | 2.45          |
| fastify-big-json         | 4.26.2  | ✓      | 13028.6    | 76.21        | 149.90        |
| express-with-middlewares | 4.19.2  | ✓      | 12997.8    | 76.35        | 4.83          |
| express-route-prefix     | 4.19.2  | ✓      | 11082.0    | 89.66        | 4.10          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Node:__ `v14.21.3`
* __Run:__ Mon Jun 05 2023 02:45:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| connect                  | 3.7.0   | ✗      | 55986.4    | 17.37        | 9.98          |
| polkadot                 | 1.0.0   | ✗      | 55549.6    | 17.52        | 9.91          |
| bare                     | 10.13.0 | ✗      | 55343.2    | 17.58        | 9.87          |
| polka                    | 0.5.2   | ✓      | 55055.2    | 17.67        | 9.82          |
| 0http                    | 3.5.2   | ✓      | 54848.8    | 17.75        | 9.78          |
| fastify                  | 4.17.0  | ✓      | 54217.6    | 17.94        | 9.72          |
| foxify                   | 0.10.20 | ✓      | 54004.8    | 18.02        | 8.86          |
| h3-router                | 0.8.6   | ✓      | 53318.4    | 18.25        | 8.75          |
| micro                    | 9.4.1   | ✗      | 53204.8    | 18.30        | 9.49          |
| h3                       | 0.8.6   | ✗      | 52528.8    | 18.55        | 8.62          |
| server-base-router       | 7.1.32  | ✓      | 51723.2    | 18.83        | 9.22          |
| yeps                     | 1.1.1   | ✗      | 51453.6    | 18.94        | 9.18          |
| server-base              | 7.1.32  | ✗      | 49140.0    | 19.85        | 8.76          |
| micro-route              | 2.5.0   | ✓      | 47119.2    | 20.74        | 8.40          |
| connect-router           | 1.3.8   | ✓      | 46957.6    | 20.80        | 8.38          |
| restana                  | 4.9.7   | ✓      | 46566.4    | 20.98        | 8.30          |
| trek-engine              | 1.0.5   | ✗      | 46369.8    | 21.07        | 7.61          |
| trek-router              | 1.2.0   | ✓      | 45740.2    | 21.37        | 7.50          |
| vapr                     | 0.6.0   | ✓      | 43634.4    | 22.42        | 7.16          |
| yeps-router              | 1.2.0   | ✓      | 40899.2    | 23.95        | 7.29          |
| koa                      | 2.14.2  | ✗      | 39845.4    | 24.59        | 7.11          |
| spirit                   | 0.6.1   | ✗      | 38124.0    | 25.74        | 6.80          |
| take-five                | 2.0.0   | ✓      | 37163.0    | 26.41        | 13.36         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36933.8    | 26.57        | 6.59          |
| restify                  | 8.6.1   | ✓      | 36758.6    | 26.70        | 6.63          |
| total.js                 | 3.4.13  | ✓      | 36428.6    | 26.95        | 11.15         |
| spirit-router            | 0.5.0   | ✓      | 36416.2    | 26.96        | 6.50          |
| koa-router               | 12.0.0  | ✓      | 34599.8    | 28.41        | 6.17          |
| hapi                     | 20.3.0  | ✓      | 29506.8    | 33.38        | 5.26          |
| microrouter              | 3.1.3   | ✓      | 29007.2    | 33.97        | 5.17          |
| trpc-router              | 9.27.3  | ✓      | 24895.2    | 39.66        | 5.51          |
| egg.js                   | 3.16.0  | ✓      | 14793.8    | 67.07        | 5.29          |
| express                  | 4.18.2  | ✓      | 12056.4    | 82.40        | 2.15          |
| express-with-middlewares | 4.18.2  | ✓      | 10671.0    | 93.17        | 3.97          |
| express-route-prefix     | 4.18.2  | ✓      | 10571.1    | 94.03        | 3.91          |
| fastify-big-json         | 4.17.0  | ✓      | 10515.1    | 94.71        | 120.98        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

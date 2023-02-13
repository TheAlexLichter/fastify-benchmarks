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
* __Node:__ `v14.21.2`
* __Run:__ Mon Feb 13 2023 02:39:50 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 56878.4    | 17.09        | 10.14         |
| fastify                  | 4.13.0  | ✓      | 55960.0    | 17.37        | 10.03         |
| polkadot                 | 1.0.0   | ✗      | 55734.4    | 17.45        | 9.94          |
| foxify                   | 0.10.20 | ✓      | 54971.2    | 17.70        | 9.02          |
| micro                    | 9.4.1   | ✗      | 54959.2    | 17.70        | 9.80          |
| polka                    | 0.5.2   | ✓      | 54606.4    | 17.82        | 9.74          |
| connect                  | 3.7.0   | ✗      | 54592.0    | 17.83        | 9.74          |
| 0http                    | 3.4.3   | ✓      | 54549.6    | 17.86        | 9.73          |
| h3                       | 0.8.6   | ✗      | 53081.6    | 18.34        | 8.71          |
| server-base              | 7.1.32  | ✗      | 52579.2    | 18.52        | 9.38          |
| h3-router                | 0.8.6   | ✓      | 51329.6    | 18.98        | 8.42          |
| server-base-router       | 7.1.32  | ✓      | 50629.6    | 19.26        | 9.03          |
| connect-router           | 1.3.7   | ✓      | 49523.2    | 19.69        | 8.83          |
| restana                  | 4.9.7   | ✓      | 49177.6    | 19.87        | 8.77          |
| yeps                     | 1.1.1   | ✗      | 49153.6    | 19.85        | 8.77          |
| micro-route              | 2.5.0   | ✓      | 47744.8    | 20.45        | 8.51          |
| trek-engine              | 1.0.5   | ✗      | 46023.4    | 21.23        | 7.55          |
| trek-router              | 1.2.0   | ✓      | 45353.0    | 21.56        | 7.44          |
| vapr                     | 0.6.0   | ✓      | 43205.6    | 22.65        | 7.09          |
| yeps-router              | 1.2.0   | ✓      | 41061.6    | 23.86        | 7.32          |
| koa                      | 2.14.1  | ✗      | 38007.0    | 25.82        | 6.78          |
| total.js                 | 3.4.13  | ✓      | 37811.0    | 25.95        | 11.58         |
| take-five                | 2.0.0   | ✓      | 37435.8    | 26.21        | 13.46         |
| spirit                   | 0.6.1   | ✗      | 37424.8    | 26.22        | 6.67          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36999.4    | 26.53        | 6.60          |
| spirit-router            | 0.5.0   | ✓      | 35949.6    | 27.33        | 6.41          |
| restify                  | 8.6.1   | ✓      | 35943.8    | 27.32        | 6.48          |
| koa-router               | 12.0.0  | ✓      | 33835.6    | 29.05        | 6.03          |
| hapi                     | 20.2.2  | ✓      | 29047.2    | 33.92        | 5.18          |
| microrouter              | 3.1.3   | ✓      | 28596.4    | 34.46        | 5.10          |
| trpc-router              | 9.27.3  | ✓      | 24283.2    | 40.67        | 5.37          |
| egg.js                   | 3.15.0  | ✓      | 15084.2    | 65.78        | 5.39          |
| express                  | 4.18.2  | ✓      | 12060.2    | 82.37        | 2.15          |
| express-with-middlewares | 4.18.2  | ✓      | 10598.6    | 93.78        | 3.94          |
| express-route-prefix     | 4.18.2  | ✓      | 10015.3    | 99.30        | 3.71          |
| fastify-big-json         | 4.13.0  | ✓      | 9836.9     | 101.16       | 113.17        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

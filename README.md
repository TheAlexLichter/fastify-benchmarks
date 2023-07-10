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
* __Run:__ Mon Jul 10 2023 02:50:33 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 55208.8    | 17.62        | 9.85          |
| bare                     | 10.13.0 | ✗      | 54622.4    | 17.84        | 9.74          |
| polka                    | 0.5.2   | ✓      | 54335.2    | 17.90        | 9.69          |
| connect                  | 3.7.0   | ✗      | 53660.0    | 18.13        | 9.57          |
| foxify                   | 0.10.20 | ✓      | 53658.4    | 18.13        | 8.80          |
| fastify                  | 4.19.2  | ✓      | 52822.4    | 18.45        | 9.47          |
| micro                    | 9.4.1   | ✗      | 52545.6    | 18.53        | 9.37          |
| 0http                    | 3.5.2   | ✓      | 52319.2    | 18.62        | 9.33          |
| server-base-router       | 7.1.32  | ✓      | 50698.4    | 19.22        | 9.04          |
| h3                       | 0.8.6   | ✗      | 50162.4    | 19.46        | 8.23          |
| h3-router                | 0.8.6   | ✓      | 49862.4    | 19.56        | 8.18          |
| server-base              | 7.1.32  | ✗      | 48781.6    | 20.00        | 8.70          |
| restana                  | 4.9.7   | ✓      | 48046.4    | 20.32        | 8.57          |
| micro-route              | 2.5.0   | ✓      | 47630.4    | 20.50        | 8.49          |
| yeps                     | 1.1.1   | ✗      | 47514.4    | 20.55        | 8.47          |
| connect-router           | 1.3.8   | ✓      | 47492.8    | 20.56        | 8.47          |
| trek-engine              | 1.0.5   | ✗      | 44465.4    | 21.99        | 7.29          |
| vapr                     | 0.6.0   | ✓      | 41911.0    | 23.38        | 6.87          |
| trek-router              | 1.2.0   | ✓      | 41878.6    | 23.38        | 6.87          |
| yeps-router              | 1.2.0   | ✓      | 40062.4    | 24.45        | 7.14          |
| koa                      | 2.14.2  | ✗      | 38503.4    | 25.47        | 6.87          |
| take-five                | 2.0.0   | ✓      | 36506.2    | 26.89        | 13.13         |
| total.js                 | 3.4.13  | ✓      | 35904.2    | 27.35        | 10.99         |
| spirit                   | 0.6.1   | ✗      | 35902.4    | 27.37        | 6.40          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 35243.0    | 27.87        | 6.28          |
| restify                  | 8.6.1   | ✓      | 34708.2    | 28.30        | 6.26          |
| spirit-router            | 0.5.0   | ✓      | 33969.4    | 28.95        | 6.06          |
| koa-router               | 12.0.0  | ✓      | 32924.2    | 29.89        | 5.87          |
| hapi                     | 20.3.0  | ✓      | 28450.0    | 34.65        | 5.07          |
| microrouter              | 3.1.3   | ✓      | 27913.6    | 35.32        | 4.98          |
| trpc-router              | 9.27.3  | ✓      | 23451.2    | 42.13        | 5.19          |
| egg.js                   | 3.17.3  | ✓      | 14084.4    | 70.52        | 5.04          |
| express                  | 4.18.2  | ✓      | 11439.4    | 86.87        | 2.04          |
| express-with-middlewares | 4.18.2  | ✓      | 9993.3     | 99.49        | 3.72          |
| express-route-prefix     | 4.18.2  | ✓      | 9654.7     | 103.02       | 3.57          |
| fastify-big-json         | 4.19.2  | ✓      | 8817.5     | 112.99       | 101.45        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

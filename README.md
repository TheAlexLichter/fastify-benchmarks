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
* __Run:__ Mon Apr 24 2023 02:28:23 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 50282.4    | 19.40        | 8.97          |
| polka                    | 0.5.2   | ✓      | 49372.8    | 19.75        | 8.80          |
| foxify                   | 0.10.20 | ✓      | 48052.8    | 20.31        | 7.88          |
| polkadot                 | 1.0.0   | ✗      | 47926.4    | 20.38        | 8.55          |
| connect                  | 3.7.0   | ✗      | 47513.6    | 20.56        | 8.47          |
| micro                    | 9.4.1   | ✗      | 47441.6    | 20.59        | 8.46          |
| fastify                  | 4.15.0  | ✓      | 46778.4    | 20.89        | 8.39          |
| 0http                    | 3.5.2   | ✓      | 46516.0    | 21.00        | 8.30          |
| h3                       | 0.8.6   | ✗      | 46435.2    | 21.04        | 7.62          |
| h3-router                | 0.8.6   | ✓      | 45789.8    | 21.36        | 7.51          |
| yeps                     | 1.1.1   | ✗      | 45424.0    | 21.52        | 8.10          |
| server-base              | 7.1.32  | ✗      | 44864.0    | 21.79        | 8.00          |
| server-base-router       | 7.1.32  | ✓      | 44824.0    | 21.82        | 7.99          |
| restana                  | 4.9.7   | ✓      | 43807.2    | 22.37        | 7.81          |
| connect-router           | 1.3.8   | ✓      | 42506.4    | 23.04        | 7.58          |
| micro-route              | 2.5.0   | ✓      | 42300.8    | 23.14        | 7.54          |
| trek-engine              | 1.0.5   | ✗      | 41111.8    | 23.83        | 6.74          |
| trek-router              | 1.2.0   | ✓      | 40787.4    | 24.03        | 6.69          |
| vapr                     | 0.6.0   | ✓      | 37774.6    | 25.98        | 6.20          |
| yeps-router              | 1.2.0   | ✓      | 36625.4    | 26.80        | 6.53          |
| koa                      | 2.14.2  | ✗      | 35990.6    | 27.29        | 6.42          |
| spirit                   | 0.6.1   | ✗      | 35839.4    | 27.43        | 6.39          |
| spirit-router            | 0.5.0   | ✓      | 33900.2    | 29.02        | 6.05          |
| take-five                | 2.0.0   | ✓      | 33393.2    | 29.45        | 12.01         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 32899.6    | 29.89        | 5.87          |
| total.js                 | 3.4.13  | ✓      | 32620.0    | 30.15        | 9.99          |
| restify                  | 8.6.1   | ✓      | 31789.4    | 30.95        | 5.73          |
| koa-router               | 12.0.0  | ✓      | 30239.6    | 32.57        | 5.39          |
| hapi                     | 20.3.0  | ✓      | 26287.1    | 37.54        | 4.69          |
| microrouter              | 3.1.3   | ✓      | 25598.8    | 38.55        | 4.56          |
| trpc-router              | 9.27.3  | ✓      | 21853.6    | 45.25        | 4.84          |
| egg.js                   | 3.15.0  | ✓      | 13053.4    | 76.07        | 4.67          |
| express                  | 4.18.2  | ✓      | 10390.0    | 95.67        | 1.85          |
| fastify-big-json         | 4.15.0  | ✓      | 9143.5     | 108.99       | 105.20        |
| express-with-middlewares | 4.18.2  | ✓      | 8993.9     | 110.58       | 3.34          |
| express-route-prefix     | 4.18.2  | ✓      | 8479.4     | 117.28       | 3.14          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

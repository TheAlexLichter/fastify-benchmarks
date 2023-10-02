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
* __Run:__ Mon Oct 02 2023 02:08:16 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 55294.4    | 17.60        | 9.86          |
| polka                    | 0.5.2   | ✓      | 53920.0    | 18.05        | 9.62          |
| foxify                   | 0.10.20 | ✓      | 53267.2    | 18.28        | 8.74          |
| micro                    | 9.4.1   | ✗      | 52972.8    | 18.38        | 9.45          |
| bare                     | 10.13.0 | ✗      | 52927.2    | 18.40        | 9.44          |
| h3                       | 0.8.6   | ✗      | 51636.8    | 18.88        | 8.47          |
| connect                  | 3.7.0   | ✗      | 51525.6    | 18.91        | 9.19          |
| fastify                  | 4.23.2  | ✓      | 51164.0    | 19.05        | 9.17          |
| h3-router                | 0.8.6   | ✓      | 50824.8    | 19.18        | 8.34          |
| server-base-router       | 7.1.32  | ✓      | 50690.4    | 19.23        | 9.04          |
| 0http                    | 3.5.2   | ✓      | 49924.8    | 19.53        | 8.90          |
| yeps                     | 1.1.1   | ✗      | 49441.6    | 19.73        | 8.82          |
| server-base              | 7.1.32  | ✗      | 48560.0    | 20.09        | 8.66          |
| restana                  | 4.9.7   | ✓      | 47898.4    | 20.39        | 8.54          |
| micro-route              | 2.5.0   | ✓      | 46226.4    | 21.14        | 8.24          |
| connect-router           | 1.3.8   | ✓      | 46188.8    | 21.16        | 8.24          |
| trek-engine              | 1.0.5   | ✗      | 45099.8    | 21.67        | 7.40          |
| trek-router              | 1.2.0   | ✓      | 44466.4    | 22.00        | 7.29          |
| vapr                     | 0.6.0   | ✓      | 41668.2    | 23.50        | 6.83          |
| yeps-router              | 1.2.0   | ✓      | 39757.4    | 24.67        | 7.09          |
| koa                      | 2.14.2  | ✗      | 38653.0    | 25.37        | 6.89          |
| spirit                   | 0.6.1   | ✗      | 37357.6    | 26.28        | 6.66          |
| spirit-router            | 0.5.0   | ✓      | 36948.0    | 26.58        | 6.59          |
| total.js                 | 3.4.13  | ✓      | 36897.4    | 26.61        | 11.30         |
| take-five                | 2.0.0   | ✓      | 36214.0    | 27.13        | 13.02         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36145.0    | 27.18        | 6.45          |
| restify                  | 8.6.1   | ✓      | 35125.6    | 27.97        | 6.33          |
| koa-router               | 12.0.0  | ✓      | 33325.2    | 29.52        | 5.94          |
| hapi                     | 20.3.0  | ✓      | 28895.6    | 34.11        | 5.15          |
| microrouter              | 3.1.3   | ✓      | 28174.0    | 35.01        | 5.02          |
| trpc-router              | 9.27.3  | ✓      | 23913.2    | 41.32        | 5.29          |
| egg.js                   | 3.17.4  | ✓      | 14315.8    | 69.31        | 5.12          |
| express                  | 4.18.2  | ✓      | 12111.4    | 82.01        | 2.16          |
| express-with-middlewares | 4.18.2  | ✓      | 10181.5    | 97.62        | 3.79          |
| fastify-big-json         | 4.23.2  | ✓      | 9729.0     | 102.34       | 111.93        |
| express-route-prefix     | 4.18.2  | ✓      | 9404.7     | 105.75       | 3.48          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

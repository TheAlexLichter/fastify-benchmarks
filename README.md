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
* __Run:__ Mon May 22 2023 02:32:35 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 57214.4    | 16.98        | 10.20         |
| polkadot                 | 1.0.0   | ✗      | 56896.0    | 17.09        | 10.15         |
| foxify                   | 0.10.20 | ✓      | 55163.2    | 17.63        | 9.05          |
| fastify                  | 4.17.0  | ✓      | 54759.2    | 17.76        | 9.82          |
| 0http                    | 3.5.2   | ✓      | 54592.0    | 17.84        | 9.74          |
| micro                    | 9.4.1   | ✗      | 54583.2    | 17.82        | 9.73          |
| connect                  | 3.7.0   | ✗      | 54487.0    | 17.87        | 9.72          |
| h3-router                | 0.8.6   | ✓      | 54332.0    | 17.90        | 8.91          |
| polka                    | 0.5.2   | ✓      | 53206.4    | 18.29        | 9.49          |
| h3                       | 0.8.6   | ✗      | 53029.6    | 18.36        | 8.70          |
| restana                  | 4.9.7   | ✓      | 50627.2    | 19.22        | 9.03          |
| yeps                     | 1.1.1   | ✗      | 50279.2    | 19.39        | 8.97          |
| server-base-router       | 7.1.32  | ✓      | 49908.8    | 19.53        | 8.90          |
| connect-router           | 1.3.8   | ✓      | 49868.0    | 19.55        | 8.89          |
| server-base              | 7.1.32  | ✗      | 49645.6    | 19.64        | 8.85          |
| micro-route              | 2.5.0   | ✓      | 48056.8    | 20.31        | 8.57          |
| trek-engine              | 1.0.5   | ✗      | 46848.6    | 20.85        | 7.68          |
| trek-router              | 1.2.0   | ✓      | 44161.4    | 22.15        | 7.24          |
| vapr                     | 0.6.0   | ✓      | 43459.2    | 22.51        | 7.13          |
| yeps-router              | 1.2.0   | ✓      | 41120.0    | 23.82        | 7.33          |
| koa                      | 2.14.2  | ✗      | 40916.8    | 23.95        | 7.30          |
| spirit                   | 0.6.1   | ✗      | 38418.4    | 25.54        | 6.85          |
| total.js                 | 3.4.13  | ✓      | 37872.6    | 25.91        | 11.59         |
| spirit-router            | 0.5.0   | ✓      | 37529.6    | 26.16        | 6.69          |
| take-five                | 2.0.0   | ✓      | 37354.6    | 26.27        | 13.43         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37184.2    | 26.39        | 6.63          |
| restify                  | 8.6.1   | ✓      | 36507.4    | 26.89        | 6.58          |
| koa-router               | 12.0.0  | ✓      | 33864.6    | 29.03        | 6.04          |
| hapi                     | 20.3.0  | ✓      | 30452.0    | 32.34        | 5.43          |
| microrouter              | 3.1.3   | ✓      | 29018.0    | 33.96        | 5.17          |
| trpc-router              | 9.27.3  | ✓      | 25339.6    | 38.96        | 5.61          |
| egg.js                   | 3.16.0  | ✓      | 15099.2    | 65.69        | 5.40          |
| express                  | 4.18.2  | ✓      | 12248.0    | 81.12        | 2.18          |
| express-route-prefix     | 4.18.2  | ✓      | 10809.0    | 91.95        | 4.00          |
| express-with-middlewares | 4.18.2  | ✓      | 10675.1    | 93.06        | 3.97          |
| fastify-big-json         | 4.17.0  | ✓      | 10529.6    | 94.52        | 121.15        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

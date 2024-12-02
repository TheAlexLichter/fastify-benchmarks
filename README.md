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
* __Run:__ Mon Dec 02 2024 02:49:48 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 70188.0    | 13.74        | 12.52         |
| 0http                    | 3.5.3   | ✓      | 69827.2    | 13.82        | 12.45         |
| h3                       | 0.8.6   | ✗      | 66547.2    | 14.53        | 10.92         |
| h3-router                | 0.8.6   | ✓      | 65291.2    | 14.82        | 10.71         |
| restana                  | 4.9.9   | ✓      | 62316.0    | 15.55        | 11.11         |
| bare                     | 10.13.0 | ✗      | 60487.2    | 16.03        | 10.79         |
| polka                    | 0.5.2   | ✓      | 58040.8    | 16.73        | 10.35         |
| foxify                   | 0.10.20 | ✓      | 57715.2    | 16.83        | 9.47          |
| connect                  | 3.7.0   | ✗      | 57491.2    | 16.90        | 10.25         |
| server-base              | 7.1.32  | ✗      | 54860.8    | 17.72        | 9.78          |
| fastify                  | 4.28.1  | ✓      | 54193.6    | 17.95        | 9.72          |
| micro                    | 9.4.1   | ✗      | 54101.6    | 17.98        | 9.65          |
| server-base-router       | 7.1.32  | ✓      | 53893.6    | 18.06        | 9.61          |
| yeps                     | 1.1.1   | ✗      | 52792.8    | 18.44        | 9.41          |
| micro-route              | 2.5.0   | ✓      | 50903.2    | 19.15        | 9.08          |
| connect-router           | 1.3.8   | ✓      | 50758.4    | 19.21        | 9.05          |
| trek-engine              | 1.0.5   | ✗      | 48688.0    | 20.04        | 7.99          |
| trek-router              | 1.2.0   | ✓      | 47101.6    | 20.73        | 7.73          |
| vapr                     | 0.6.0   | ✓      | 46146.4    | 21.17        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 44705.6    | 21.89        | 7.97          |
| yeps-router              | 1.2.0   | ✓      | 44071.2    | 22.19        | 7.86          |
| spirit-router            | 0.5.0   | ✓      | 43600.0    | 22.42        | 7.78          |
| koa                      | 2.15.3  | ✗      | 42772.8    | 22.89        | 7.63          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40111.2    | 24.44        | 7.15          |
| total.js                 | 3.4.13  | ✓      | 39662.4    | 24.71        | 12.14         |
| restify                  | 8.6.1   | ✓      | 39468.0    | 24.84        | 7.11          |
| take-five                | 2.0.0   | ✓      | 38375.4    | 25.57        | 13.80         |
| koa-router               | 12.0.1  | ✓      | 37767.0    | 25.97        | 6.74          |
| hapi                     | 20.3.0  | ✓      | 33665.4    | 29.20        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 31823.6    | 30.92        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 26808.4    | 36.79        | 5.93          |
| egg.js                   | 3.29.0  | ✓      | 17603.0    | 56.29        | 6.30          |
| express                  | 4.21.1  | ✓      | 13404.4    | 74.06        | 2.39          |
| fastify-big-json         | 4.28.1  | ✓      | 12822.0    | 77.44        | 147.52        |
| express-with-middlewares | 4.21.1  | ✓      | 12406.4    | 80.04        | 4.61          |
| express-route-prefix     | 4.21.1  | ✓      | 10908.2    | 91.11        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

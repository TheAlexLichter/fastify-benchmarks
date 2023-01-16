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
* __Run:__ Mon Jan 16 2023 02:33:12 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 59186.4    | 16.40        | 10.55         |
| bare                     | 10.13.0 | ✗      | 56902.4    | 17.08        | 10.15         |
| foxify                   | 0.10.20 | ✓      | 56660.0    | 17.15        | 9.29          |
| fastify                  | 4.11.0  | ✓      | 56178.4    | 17.31        | 10.07         |
| 0http                    | 3.4.2   | ✓      | 55808.0    | 17.41        | 9.95          |
| micro                    | 9.4.1   | ✗      | 55680.8    | 17.48        | 9.93          |
| connect                  | 3.7.0   | ✗      | 55629.8    | 17.49        | 9.92          |
| h3                       | 0.8.6   | ✗      | 54878.4    | 17.73        | 9.00          |
| h3-router                | 0.8.6   | ✓      | 54649.6    | 17.80        | 8.96          |
| server-base              | 7.1.32  | ✗      | 54116.0    | 17.97        | 9.65          |
| polka                    | 0.5.2   | ✓      | 53520.0    | 18.19        | 9.54          |
| server-base-router       | 7.1.32  | ✓      | 53428.0    | 18.23        | 9.53          |
| yeps                     | 1.1.1   | ✗      | 51185.6    | 19.04        | 9.13          |
| connect-router           | 1.3.7   | ✓      | 50344.0    | 19.36        | 8.98          |
| restana                  | 4.9.7   | ✓      | 50109.6    | 19.51        | 8.94          |
| micro-route              | 2.5.0   | ✓      | 48861.6    | 19.97        | 8.71          |
| trek-engine              | 1.0.5   | ✗      | 46163.0    | 21.17        | 7.57          |
| trek-router              | 1.2.0   | ✓      | 45967.4    | 21.26        | 7.54          |
| vapr                     | 0.6.0   | ✓      | 44155.2    | 22.16        | 7.24          |
| yeps-router              | 1.2.0   | ✓      | 41905.6    | 23.37        | 7.47          |
| koa                      | 2.14.1  | ✗      | 41837.4    | 23.41        | 7.46          |
| spirit                   | 0.6.1   | ✗      | 39742.4    | 24.67        | 7.09          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39026.6    | 25.12        | 6.96          |
| spirit-router            | 0.5.0   | ✓      | 38440.0    | 25.52        | 6.86          |
| take-five                | 2.0.0   | ✓      | 38095.8    | 25.75        | 13.70         |
| total.js                 | 3.4.13  | ✓      | 37388.8    | 26.25        | 11.45         |
| restify                  | 8.6.1   | ✓      | 37281.0    | 26.33        | 6.72          |
| koa-router               | 12.0.0  | ✓      | 34574.6    | 28.42        | 6.17          |
| hapi                     | 20.2.2  | ✓      | 30112.0    | 32.71        | 5.37          |
| microrouter              | 3.1.3   | ✓      | 28750.0    | 34.28        | 5.13          |
| trpc-router              | 9.27.3  | ✓      | 22830.0    | 43.29        | 5.05          |
| egg.js                   | 3.13.0  | ✓      | 15286.2    | 64.89        | 5.47          |
| express                  | 4.18.2  | ✓      | 12288.8    | 80.90        | 2.19          |
| express-with-middlewares | 4.18.2  | ✓      | 10647.6    | 93.35        | 3.96          |
| express-route-prefix     | 4.18.2  | ✓      | 10562.0    | 94.07        | 3.91          |
| fastify-big-json         | 4.11.0  | ✓      | 10323.4    | 96.38        | 118.78        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

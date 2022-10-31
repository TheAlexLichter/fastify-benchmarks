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
* __Node:__ `v14.20.1`
* __Run:__ Mon Oct 31 2022 03:27:05 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 31856.2    | 30.94        | 5.68          |
| 0http                    | 3.4.1   | ✓      | 31788.0    | 30.97        | 5.67          |
| h3-router                | 0.8.6   | ✓      | 31213.4    | 31.56        | 5.12          |
| bare                     | 10.13.0 | ✗      | 30502.0    | 32.34        | 5.44          |
| foxify                   | 0.10.20 | ✓      | 30381.8    | 32.42        | 4.98          |
| micro                    | 9.4.1   | ✗      | 30286.6    | 32.52        | 5.40          |
| fastify                  | 4.9.2   | ✓      | 29886.8    | 32.98        | 5.36          |
| h3                       | 0.8.6   | ✗      | 29865.6    | 33.02        | 4.90          |
| polka                    | 0.5.2   | ✓      | 28399.6    | 34.73        | 5.06          |
| server-base              | 7.1.32  | ✗      | 27402.8    | 36.03        | 4.89          |
| rayo                     | 1.3.10  | ✓      | 27371.6    | 36.05        | 4.88          |
| connect                  | 3.7.0   | ✗      | 27256.8    | 36.20        | 4.86          |
| yeps                     | 1.1.1   | ✗      | 27037.6    | 36.47        | 4.82          |
| server-base-router       | 7.1.32  | ✓      | 26332.4    | 37.47        | 4.70          |
| spirit                   | 0.6.1   | ✗      | 26155.6    | 37.81        | 4.66          |
| micro-route              | 2.5.0   | ✓      | 25670.8    | 38.46        | 4.58          |
| trek-engine              | 1.0.5   | ✗      | 25231.2    | 39.14        | 4.14          |
| trek-router              | 1.2.0   | ✓      | 25122.8    | 39.32        | 4.12          |
| spirit-router            | 0.5.0   | ✓      | 24963.2    | 39.62        | 4.45          |
| connect-router           | 1.3.7   | ✓      | 24017.6    | 41.14        | 4.28          |
| yeps-router              | 1.2.0   | ✓      | 23358.4    | 42.30        | 4.17          |
| vapr                     | 0.6.0   | ✓      | 22580.4    | 43.77        | 3.70          |
| koa                      | 2.13.4  | ✗      | 22360.8    | 44.23        | 3.99          |
| restana                  | 4.9.6   | ✓      | 21178.4    | 46.72        | 3.78          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20508.5    | 48.26        | 3.66          |
| restify                  | 8.6.1   | ✓      | 19872.1    | 49.82        | 3.58          |
| total.js                 | 3.4.13  | ✓      | 19444.9    | 50.90        | 5.95          |
| take-five                | 2.0.0   | ✓      | 19282.7    | 51.35        | 6.93          |
| koa-router               | 12.0.0  | ✓      | 18916.9    | 52.37        | 3.37          |
| hapi                     | 20.2.2  | ✓      | 18669.1    | 53.05        | 3.33          |
| trpc-router              | 9.27.4  | ✓      | 17563.8    | 56.44        | 3.89          |
| microrouter              | 3.1.3   | ✓      | 16815.6    | 58.96        | 3.00          |
| egg.js                   | 3.3.3   | ✓      | 10870.2    | 91.49        | 3.89          |
| express                  | 4.18.2  | ✓      | 7527.6     | 132.24       | 1.34          |
| express-route-prefix     | 4.18.2  | ✓      | 6774.7     | 146.98       | 2.51          |
| fastify-big-json         | 4.9.2   | ✓      | 6723.5     | 148.20       | 77.35         |
| express-with-middlewares | 4.18.2  | ✓      | 6572.7     | 151.44       | 2.44          |

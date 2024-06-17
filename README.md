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
* __Run:__ Mon Jun 17 2024 02:25:20 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69530.8    | 13.89        | 12.40         |
| polkadot                 | 1.0.0   | ✗      | 67816.8    | 14.25        | 12.09         |
| h3-router                | 0.8.6   | ✓      | 66486.8    | 14.55        | 10.91         |
| h3                       | 0.8.6   | ✗      | 66210.0    | 14.60        | 10.86         |
| restana                  | 4.9.9   | ✓      | 61804.0    | 15.68        | 11.02         |
| bare                     | 10.13.0 | ✗      | 60240.8    | 16.09        | 10.74         |
| foxify                   | 0.10.20 | ✓      | 59725.6    | 16.24        | 9.80          |
| polka                    | 0.5.2   | ✓      | 57932.8    | 16.78        | 10.33         |
| fastify                  | 4.28.0  | ✓      | 57170.4    | 16.99        | 10.25         |
| micro                    | 9.4.1   | ✗      | 56495.2    | 17.20        | 10.08         |
| connect                  | 3.7.0   | ✗      | 55971.2    | 17.35        | 9.98          |
| server-base              | 7.1.32  | ✗      | 53973.6    | 18.03        | 9.63          |
| server-base-router       | 7.1.32  | ✓      | 53540.8    | 18.18        | 9.55          |
| yeps                     | 1.1.1   | ✗      | 52057.6    | 18.72        | 9.28          |
| micro-route              | 2.5.0   | ✓      | 50888.0    | 19.16        | 9.08          |
| connect-router           | 1.3.8   | ✓      | 49948.8    | 19.53        | 8.91          |
| trek-engine              | 1.0.5   | ✗      | 49562.4    | 19.68        | 8.13          |
| trek-router              | 1.2.0   | ✓      | 48356.0    | 20.18        | 7.93          |
| vapr                     | 0.6.0   | ✓      | 46172.0    | 21.16        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 45163.2    | 21.68        | 8.05          |
| yeps-router              | 1.2.0   | ✓      | 44493.6    | 21.99        | 7.93          |
| koa                      | 2.15.3  | ✗      | 42954.4    | 22.78        | 7.66          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39623.8    | 24.73        | 7.07          |
| total.js                 | 3.4.13  | ✓      | 39356.0    | 24.92        | 12.05         |
| restify                  | 8.6.1   | ✓      | 39032.6    | 25.13        | 7.04          |
| take-five                | 2.0.0   | ✓      | 38821.0    | 25.25        | 13.96         |
| koa-router               | 12.0.1  | ✓      | 37683.8    | 26.04        | 6.72          |
| spirit-router            | 0.5.0   | ✓      | 36280.0    | 27.07        | 6.47          |
| hapi                     | 20.3.0  | ✓      | 34113.8    | 28.80        | 6.08          |
| microrouter              | 3.1.3   | ✓      | 32691.4    | 30.08        | 5.83          |
| trpc-router              | 9.27.4  | ✓      | 26971.2    | 36.57        | 5.97          |
| egg.js                   | 3.24.1  | ✓      | 17258.5    | 57.43        | 6.17          |
| express                  | 4.19.2  | ✓      | 13628.2    | 72.82        | 2.43          |
| fastify-big-json         | 4.28.0  | ✓      | 12896.4    | 77.00        | 148.38        |
| express-with-middlewares | 4.19.2  | ✓      | 12665.4    | 78.40        | 4.71          |
| express-route-prefix     | 4.19.2  | ✓      | 10929.8    | 90.91        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jan 15 2024 02:15:05 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.2   | ✓      | 66323.6    | 14.58        | 11.83         |
| polkadot                 | 1.0.0   | ✗      | 65565.2    | 14.77        | 11.69         |
| h3                       | 0.8.6   | ✗      | 64161.2    | 15.10        | 10.53         |
| h3-router                | 0.8.6   | ✓      | 61341.6    | 15.82        | 10.06         |
| bare                     | 10.13.0 | ✗      | 61027.2    | 15.90        | 10.88         |
| foxify                   | 0.10.20 | ✓      | 60241.6    | 16.10        | 9.88          |
| fastify                  | 4.25.2  | ✓      | 58100.8    | 16.72        | 10.42         |
| polka                    | 0.5.2   | ✓      | 57512.0    | 16.89        | 10.26         |
| connect                  | 3.7.0   | ✗      | 57492.8    | 16.90        | 10.25         |
| micro                    | 9.4.1   | ✗      | 56508.8    | 17.20        | 10.08         |
| restana                  | 4.9.7   | ✓      | 54549.6    | 17.88        | 9.73          |
| server-base-router       | 7.1.32  | ✓      | 53866.4    | 18.07        | 9.61          |
| server-base              | 7.1.32  | ✗      | 52664.0    | 18.49        | 9.39          |
| yeps                     | 1.1.1   | ✗      | 50447.2    | 19.32        | 9.00          |
| micro-route              | 2.5.0   | ✓      | 49771.2    | 19.60        | 8.88          |
| connect-router           | 1.3.8   | ✓      | 48871.2    | 19.97        | 8.72          |
| trek-engine              | 1.0.5   | ✗      | 48779.2    | 20.00        | 8.00          |
| trek-router              | 1.2.0   | ✓      | 47816.0    | 20.42        | 7.84          |
| vapr                     | 0.6.0   | ✓      | 46180.8    | 21.16        | 7.57          |
| koa                      | 2.15.0  | ✗      | 42229.6    | 23.18        | 7.53          |
| yeps-router              | 1.2.0   | ✓      | 41856.8    | 23.40        | 7.47          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38971.8    | 25.17        | 6.95          |
| spirit                   | 0.6.1   | ✗      | 38838.4    | 25.25        | 6.93          |
| total.js                 | 3.4.13  | ✓      | 38668.8    | 25.36        | 11.84         |
| take-five                | 2.0.0   | ✓      | 38550.6    | 25.44        | 13.86         |
| restify                  | 8.6.1   | ✓      | 37919.4    | 25.87        | 6.83          |
| spirit-router            | 0.5.0   | ✓      | 37383.2    | 26.27        | 6.67          |
| koa-router               | 12.0.1  | ✓      | 36969.8    | 26.55        | 6.59          |
| hapi                     | 20.3.0  | ✓      | 33424.6    | 29.42        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 30986.4    | 31.77        | 5.53          |
| trpc-router              | 9.27.4  | ✓      | 26079.6    | 37.83        | 5.77          |
| egg.js                   | 3.17.7  | ✓      | 18042.0    | 54.91        | 6.45          |
| express                  | 4.18.2  | ✓      | 13721.0    | 72.34        | 2.45          |
| express-with-middlewares | 4.18.2  | ✓      | 12610.2    | 78.74        | 4.69          |
| fastify-big-json         | 4.25.2  | ✓      | 12486.8    | 79.55        | 143.68        |
| express-route-prefix     | 4.18.2  | ✓      | 10924.8    | 90.96        | 4.04          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

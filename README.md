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
* __Run:__ Mon Jul 13 2026 04:34:09 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 73832.4    | 13.06        | 13.17         |
| bare                     | 10.13.0 | ✗      | 72179.6    | 13.36        | 12.87         |
| polka                    | 0.5.2   | ✓      | 71449.2    | 13.50        | 12.74         |
| h3                       | 0.8.6   | ✗      | 70538.8    | 13.66        | 11.57         |
| connect                  | 3.7.0   | ✗      | 69058.8    | 13.98        | 12.32         |
| restana                  | 4.9.9   | ✓      | 68214.0    | 14.18        | 12.17         |
| h3-router                | 0.8.6   | ✓      | 68089.6    | 14.19        | 11.17         |
| polkadot                 | 1.0.0   | ✗      | 67822.4    | 14.25        | 12.09         |
| foxify                   | 0.10.20 | ✓      | 67359.2    | 14.35        | 11.05         |
| fastify                  | 4.29.1  | ✓      | 66558.4    | 14.53        | 11.93         |
| micro                    | 9.4.1   | ✗      | 66090.8    | 14.63        | 11.79         |
| server-base              | 7.1.32  | ✗      | 65955.2    | 14.66        | 11.76         |
| server-base-router       | 7.1.32  | ✓      | 65857.6    | 14.69        | 11.74         |
| yeps                     | 1.1.1   | ✗      | 64714.4    | 14.95        | 11.54         |
| connect-router           | 1.3.8   | ✓      | 63073.2    | 15.36        | 11.25         |
| micro-route              | 2.5.0   | ✓      | 58994.4    | 16.45        | 10.52         |
| vapr                     | 0.6.0   | ✓      | 57286.4    | 16.96        | 9.40          |
| trek-engine              | 1.0.5   | ✗      | 54744.8    | 17.77        | 8.98          |
| trek-router              | 1.2.0   | ✓      | 54316.8    | 17.91        | 8.91          |
| yeps-router              | 1.2.0   | ✓      | 51600.8    | 18.89        | 9.20          |
| total.js                 | 3.4.13  | ✓      | 51529.6    | 18.91        | 15.77         |
| take-five                | 2.0.0   | ✓      | 50473.6    | 19.31        | 18.15         |
| koa                      | 2.16.4  | ✗      | 50228.8    | 19.41        | 8.96          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 46244.8    | 21.14        | 8.25          |
| restify                  | 8.6.1   | ✓      | 45268.0    | 21.60        | 8.16          |
| spirit                   | 0.6.1   | ✗      | 44413.6    | 21.94        | 7.92          |
| koa-router               | 12.0.1  | ✓      | 44140.8    | 22.15        | 7.87          |
| spirit-router            | 0.5.0   | ✓      | 42709.6    | 22.93        | 7.62          |
| microrouter              | 3.1.3   | ✓      | 40709.8    | 24.07        | 7.26          |
| hapi                     | 20.3.0  | ✓      | 39131.0    | 25.06        | 6.98          |
| trpc-router              | 9.27.4  | ✓      | 31869.2    | 30.88        | 7.05          |
| egg.js                   | 3.34.0  | ✓      | 18778.1    | 52.73        | 6.72          |
| express                  | 4.22.2  | ✓      | 16174.0    | 61.30        | 2.88          |
| express-with-middlewares | 4.22.2  | ✓      | 15434.6    | 64.26        | 5.74          |
| fastify-big-json         | 4.29.1  | ✓      | 12840.0    | 77.34        | 147.74        |
| express-route-prefix     | 4.22.2  | ✓      | 12385.0    | 80.17        | 4.58          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

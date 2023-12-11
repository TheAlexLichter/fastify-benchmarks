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
* __Run:__ Mon Dec 11 2023 02:12:40 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69795.6    | 13.83        | 12.45         |
| h3                       | 0.8.6   | ✗      | 67344.4    | 14.37        | 11.05         |
| h3-router                | 0.8.6   | ✓      | 66311.2    | 14.57        | 10.88         |
| 0http                    | 3.5.2   | ✓      | 65997.6    | 14.66        | 11.77         |
| bare                     | 10.13.0 | ✗      | 60929.6    | 15.91        | 10.87         |
| foxify                   | 0.10.20 | ✓      | 60109.6    | 16.13        | 9.86          |
| polka                    | 0.5.2   | ✓      | 58197.6    | 16.70        | 10.38         |
| connect                  | 3.7.0   | ✗      | 57117.6    | 17.01        | 10.19         |
| micro                    | 9.4.1   | ✗      | 56038.4    | 17.34        | 9.99          |
| restana                  | 4.9.7   | ✓      | 55946.4    | 17.39        | 9.98          |
| fastify                  | 4.24.3  | ✓      | 55890.4    | 17.39        | 10.02         |
| server-base              | 7.1.32  | ✗      | 55652.0    | 17.47        | 9.93          |
| server-base-router       | 7.1.32  | ✓      | 53635.2    | 18.14        | 9.57          |
| yeps                     | 1.1.1   | ✗      | 51839.2    | 18.81        | 9.24          |
| micro-route              | 2.5.0   | ✓      | 50290.4    | 19.40        | 8.97          |
| connect-router           | 1.3.8   | ✓      | 50226.4    | 19.41        | 8.96          |
| trek-engine              | 1.0.5   | ✗      | 48240.8    | 20.24        | 7.91          |
| trek-router              | 1.2.0   | ✓      | 47108.6    | 20.73        | 7.73          |
| vapr                     | 0.6.0   | ✓      | 46016.8    | 21.22        | 7.55          |
| spirit                   | 0.6.1   | ✗      | 44282.4    | 22.12        | 7.90          |
| yeps-router              | 1.2.0   | ✓      | 43307.2    | 22.60        | 7.72          |
| spirit-router            | 0.5.0   | ✓      | 42866.4    | 22.80        | 7.64          |
| koa                      | 2.14.2  | ✗      | 42692.8    | 22.92        | 7.61          |
| total.js                 | 3.4.13  | ✓      | 39920.0    | 24.55        | 12.22         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39614.4    | 24.74        | 7.06          |
| restify                  | 8.6.1   | ✓      | 39559.2    | 24.77        | 7.13          |
| take-five                | 2.0.0   | ✓      | 38669.0    | 25.35        | 13.90         |
| koa-router               | 12.0.1  | ✓      | 36681.8    | 26.76        | 6.54          |
| hapi                     | 20.3.0  | ✓      | 34126.2    | 28.80        | 6.09          |
| microrouter              | 3.1.3   | ✓      | 32066.2    | 30.67        | 5.72          |
| trpc-router              | 9.27.3  | ✓      | 26617.2    | 37.06        | 5.89          |
| egg.js                   | 3.17.5  | ✓      | 17749.0    | 55.84        | 6.35          |
| express                  | 4.18.2  | ✓      | 13459.8    | 73.74        | 2.40          |
| fastify-big-json         | 4.24.3  | ✓      | 13003.6    | 76.36        | 149.61        |
| express-with-middlewares | 4.18.2  | ✓      | 12515.0    | 79.36        | 4.65          |
| express-route-prefix     | 4.18.2  | ✓      | 11031.4    | 90.08        | 4.08          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

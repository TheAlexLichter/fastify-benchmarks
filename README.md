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
* __Run:__ Mon Jun 12 2023 02:45:18 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 58266.4    | 16.68        | 10.39         |
| polkadot                 | 1.0.0   | ✗      | 57548.8    | 16.88        | 10.26         |
| polka                    | 0.5.2   | ✓      | 56819.2    | 17.11        | 10.13         |
| micro                    | 9.4.1   | ✗      | 55726.4    | 17.45        | 9.94          |
| h3                       | 0.8.6   | ✗      | 55693.6    | 17.47        | 9.13          |
| connect                  | 3.7.0   | ✗      | 55491.2    | 17.52        | 9.90          |
| 0http                    | 3.5.2   | ✓      | 55268.0    | 17.62        | 9.86          |
| h3-router                | 0.8.6   | ✓      | 54795.2    | 17.75        | 8.99          |
| foxify                   | 0.10.20 | ✓      | 54232.8    | 17.94        | 8.90          |
| server-base              | 7.1.32  | ✗      | 53049.6    | 18.35        | 9.46          |
| fastify                  | 4.18.0  | ✓      | 52997.6    | 18.37        | 9.50          |
| server-base-router       | 7.1.32  | ✓      | 52082.4    | 18.71        | 9.29          |
| yeps                     | 1.1.1   | ✗      | 51268.0    | 19.01        | 9.14          |
| connect-router           | 1.3.8   | ✓      | 49737.6    | 19.61        | 8.87          |
| micro-route              | 2.5.0   | ✓      | 48383.2    | 20.17        | 8.63          |
| restana                  | 4.9.7   | ✓      | 48328.8    | 20.26        | 8.62          |
| trek-engine              | 1.0.5   | ✗      | 46922.4    | 20.82        | 7.70          |
| trek-router              | 1.2.0   | ✓      | 46517.8    | 21.01        | 7.63          |
| vapr                     | 0.6.0   | ✓      | 43692.8    | 22.39        | 7.17          |
| yeps-router              | 1.2.0   | ✓      | 41495.2    | 23.60        | 7.40          |
| koa                      | 2.14.2  | ✗      | 41261.6    | 23.74        | 7.36          |
| spirit                   | 0.6.1   | ✗      | 40204.0    | 24.39        | 7.17          |
| spirit-router            | 0.5.0   | ✓      | 39040.8    | 25.12        | 6.96          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38018.6    | 25.80        | 6.78          |
| total.js                 | 3.4.13  | ✓      | 37410.6    | 26.23        | 11.45         |
| take-five                | 2.0.0   | ✓      | 37295.0    | 26.31        | 13.41         |
| restify                  | 8.6.1   | ✓      | 36545.0    | 26.86        | 6.59          |
| koa-router               | 12.0.0  | ✓      | 34808.6    | 28.23        | 6.21          |
| hapi                     | 20.3.0  | ✓      | 30731.6    | 32.04        | 5.48          |
| microrouter              | 3.1.3   | ✓      | 29660.4    | 33.21        | 5.29          |
| trpc-router              | 9.27.3  | ✓      | 25117.2    | 39.30        | 5.56          |
| egg.js                   | 3.16.0  | ✓      | 14691.4    | 67.54        | 5.25          |
| express                  | 4.18.2  | ✓      | 12074.6    | 82.26        | 2.15          |
| fastify-big-json         | 4.18.0  | ✓      | 10454.5    | 95.21        | 120.27        |
| express-with-middlewares | 4.18.2  | ✓      | 10452.5    | 95.10        | 3.89          |
| express-route-prefix     | 4.18.2  | ✓      | 9690.6     | 102.65       | 3.59          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jan 08 2024 02:12:36 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.2   | ✓      | 63342.4    | 15.30        | 11.30         |
| polkadot                 | 1.0.0   | ✗      | 63225.2    | 15.32        | 11.28         |
| h3-router                | 0.8.6   | ✓      | 60266.4    | 16.11        | 9.89          |
| bare                     | 10.13.0 | ✗      | 60040.8    | 16.16        | 10.71         |
| h3                       | 0.8.6   | ✗      | 59413.6    | 16.34        | 9.75          |
| foxify                   | 0.10.20 | ✓      | 58912.8    | 16.47        | 9.66          |
| polka                    | 0.5.2   | ✓      | 57453.6    | 16.91        | 10.25         |
| fastify                  | 4.25.2  | ✓      | 57030.4    | 17.04        | 10.22         |
| connect                  | 3.7.0   | ✗      | 56072.8    | 17.34        | 10.00         |
| restana                  | 4.9.7   | ✓      | 54638.4    | 17.81        | 9.74          |
| micro                    | 9.4.1   | ✗      | 54543.2    | 17.83        | 9.73          |
| server-base              | 7.1.32  | ✗      | 53890.4    | 18.06        | 9.61          |
| server-base-router       | 7.1.32  | ✓      | 53368.0    | 18.24        | 9.52          |
| yeps                     | 1.1.1   | ✗      | 49866.4    | 19.55        | 8.89          |
| connect-router           | 1.3.8   | ✓      | 49459.2    | 19.72        | 8.82          |
| micro-route              | 2.5.0   | ✓      | 48784.8    | 19.99        | 8.70          |
| trek-engine              | 1.0.5   | ✗      | 46744.8    | 20.90        | 7.67          |
| trek-router              | 1.2.0   | ✓      | 46362.4    | 21.07        | 7.60          |
| vapr                     | 0.6.0   | ✓      | 44200.8    | 22.13        | 7.25          |
| yeps-router              | 1.2.0   | ✓      | 43423.2    | 22.53        | 7.74          |
| koa                      | 2.15.0  | ✗      | 41115.4    | 23.83        | 7.33          |
| spirit                   | 0.6.1   | ✗      | 40548.0    | 24.20        | 7.23          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38698.4    | 25.34        | 6.90          |
| total.js                 | 3.4.13  | ✓      | 38547.2    | 25.44        | 11.80         |
| take-five                | 2.0.0   | ✓      | 37939.4    | 25.85        | 13.64         |
| restify                  | 8.6.1   | ✓      | 37547.8    | 26.13        | 6.77          |
| spirit-router            | 0.5.0   | ✓      | 37074.4    | 26.46        | 6.61          |
| koa-router               | 12.0.1  | ✓      | 36753.8    | 26.70        | 6.55          |
| hapi                     | 20.3.0  | ✓      | 32706.4    | 30.07        | 5.83          |
| microrouter              | 3.1.3   | ✓      | 31582.2    | 31.17        | 5.63          |
| trpc-router              | 9.27.4  | ✓      | 25959.6    | 38.01        | 5.74          |
| egg.js                   | 3.17.5  | ✓      | 17216.7    | 57.57        | 6.16          |
| express                  | 4.18.2  | ✓      | 13008.6    | 76.32        | 2.32          |
| fastify-big-json         | 4.25.2  | ✓      | 12603.0    | 78.81        | 145.01        |
| express-with-middlewares | 4.18.2  | ✓      | 12477.8    | 79.59        | 4.64          |
| express-route-prefix     | 4.18.2  | ✓      | 10937.0    | 90.87        | 4.05          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jun 23 2025 03:12:15 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68806.8    | 14.03        | 12.27         |
| polkadot                 | 1.0.0   | ✗      | 68273.2    | 14.15        | 12.18         |
| h3-router                | 0.8.6   | ✓      | 63465.2    | 15.26        | 10.41         |
| h3                       | 0.8.6   | ✗      | 62716.0    | 15.45        | 10.29         |
| bare                     | 10.13.0 | ✗      | 59601.6    | 16.28        | 10.63         |
| foxify                   | 0.10.20 | ✓      | 58038.4    | 16.73        | 9.52          |
| restana                  | 4.9.9   | ✓      | 57535.2    | 16.89        | 10.26         |
| polka                    | 0.5.2   | ✓      | 57257.6    | 16.97        | 10.21         |
| connect                  | 3.7.0   | ✗      | 55887.2    | 17.40        | 9.97          |
| micro                    | 9.4.1   | ✗      | 55227.2    | 17.61        | 9.85          |
| server-base-router       | 7.1.32  | ✓      | 54134.4    | 17.97        | 9.65          |
| server-base              | 7.1.32  | ✗      | 53232.8    | 18.28        | 9.49          |
| fastify                  | 4.29.1  | ✓      | 52693.6    | 18.48        | 9.45          |
| yeps                     | 1.1.1   | ✗      | 51442.4    | 18.94        | 9.17          |
| connect-router           | 1.3.8   | ✓      | 49834.4    | 19.57        | 8.89          |
| micro-route              | 2.5.0   | ✓      | 48636.0    | 20.06        | 8.67          |
| trek-engine              | 1.0.5   | ✗      | 47291.2    | 20.65        | 7.76          |
| trek-router              | 1.2.0   | ✓      | 45935.2    | 21.27        | 7.54          |
| vapr                     | 0.6.0   | ✓      | 44686.4    | 21.89        | 7.33          |
| spirit                   | 0.6.1   | ✗      | 43829.6    | 22.33        | 7.82          |
| yeps-router              | 1.2.0   | ✓      | 43070.4    | 22.71        | 7.68          |
| koa                      | 2.16.1  | ✗      | 41122.4    | 23.82        | 7.33          |
| spirit-router            | 0.5.0   | ✓      | 38589.6    | 25.42        | 6.88          |
| total.js                 | 3.4.13  | ✓      | 38211.4    | 25.67        | 11.70         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38187.8    | 25.69        | 6.81          |
| take-five                | 2.0.0   | ✓      | 38085.8    | 25.75        | 13.69         |
| restify                  | 8.6.1   | ✓      | 37462.6    | 26.19        | 6.75          |
| koa-router               | 12.0.1  | ✓      | 35479.0    | 27.69        | 6.33          |
| hapi                     | 20.3.0  | ✓      | 32277.8    | 30.48        | 5.76          |
| microrouter              | 3.1.3   | ✓      | 31724.4    | 31.01        | 5.66          |
| trpc-router              | 9.27.4  | ✓      | 26678.8    | 36.98        | 5.90          |
| egg.js                   | 3.30.1  | ✓      | 16945.3    | 58.48        | 6.06          |
| express                  | 4.21.2  | ✓      | 13061.2    | 76.02        | 2.33          |
| fastify-big-json         | 4.29.1  | ✓      | 12413.2    | 80.03        | 142.82        |
| express-with-middlewares | 4.21.2  | ✓      | 12352.2    | 80.40        | 4.59          |
| express-route-prefix     | 4.21.2  | ✓      | 10657.5    | 93.24        | 3.94          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

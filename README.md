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
* __Run:__ Mon Dec 01 2025 03:22:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68237.2    | 14.16        | 12.17         |
| polkadot                 | 1.0.0   | ✗      | 66361.2    | 14.58        | 11.83         |
| h3                       | 0.8.6   | ✗      | 65937.2    | 14.67        | 10.82         |
| h3-router                | 0.8.6   | ✓      | 63365.2    | 15.29        | 10.39         |
| foxify                   | 0.10.20 | ✓      | 60213.6    | 16.11        | 9.88          |
| bare                     | 10.13.0 | ✗      | 59019.2    | 16.44        | 10.52         |
| polka                    | 0.5.2   | ✓      | 58700.8    | 16.53        | 10.47         |
| connect                  | 3.7.0   | ✗      | 57403.2    | 16.93        | 10.24         |
| restana                  | 4.9.9   | ✓      | 57128.8    | 17.01        | 10.19         |
| micro                    | 9.4.1   | ✗      | 56739.2    | 17.13        | 10.12         |
| fastify                  | 4.29.1  | ✓      | 56342.4    | 17.25        | 10.10         |
| server-base              | 7.1.32  | ✗      | 55294.4    | 17.59        | 9.86          |
| server-base-router       | 7.1.32  | ✓      | 55182.4    | 17.62        | 9.84          |
| yeps                     | 1.1.1   | ✗      | 54151.2    | 17.97        | 9.66          |
| connect-router           | 1.3.8   | ✓      | 50425.6    | 19.34        | 8.99          |
| micro-route              | 2.5.0   | ✓      | 49545.6    | 19.69        | 8.84          |
| trek-engine              | 1.0.5   | ✗      | 47119.2    | 20.72        | 7.73          |
| trek-router              | 1.2.0   | ✓      | 46262.4    | 21.11        | 7.59          |
| vapr                     | 0.6.0   | ✓      | 45603.2    | 21.43        | 7.48          |
| yeps-router              | 1.2.0   | ✓      | 44163.2    | 22.15        | 7.88          |
| spirit                   | 0.6.1   | ✗      | 43528.0    | 22.48        | 7.76          |
| koa                      | 2.16.3  | ✗      | 41607.2    | 23.53        | 7.42          |
| spirit-router            | 0.5.0   | ✓      | 40660.0    | 24.09        | 7.25          |
| total.js                 | 3.4.13  | ✓      | 39870.4    | 24.58        | 12.21         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39107.8    | 25.07        | 6.97          |
| restify                  | 8.6.1   | ✓      | 38313.8    | 25.61        | 6.91          |
| take-five                | 2.0.0   | ✓      | 38254.6    | 25.64        | 13.76         |
| koa-router               | 12.0.1  | ✓      | 36662.6    | 26.78        | 6.54          |
| hapi                     | 20.3.0  | ✓      | 32916.0    | 29.88        | 5.87          |
| microrouter              | 3.1.3   | ✓      | 31835.0    | 30.92        | 5.68          |
| trpc-router              | 9.27.4  | ✓      | 26703.2    | 36.94        | 5.91          |
| egg.js                   | 3.31.0  | ✓      | 16976.6    | 58.39        | 6.07          |
| express                  | 4.21.2  | ✓      | 13297.6    | 74.67        | 2.37          |
| fastify-big-json         | 4.29.1  | ✓      | 12624.0    | 78.67        | 145.26        |
| express-with-middlewares | 4.21.2  | ✓      | 12326.6    | 80.57        | 4.58          |
| express-route-prefix     | 4.21.2  | ✓      | 10912.4    | 91.06        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

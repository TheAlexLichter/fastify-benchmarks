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
* __Node:__ `v14.21.1`
* __Run:__ Mon Dec 19 2022 02:27:13 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 50164.8    | 19.44        | 8.95          |
| bare                     | 10.13.0 | ✗      | 49096.0    | 19.88        | 8.76          |
| micro                    | 9.4.1   | ✗      | 48986.4    | 19.92        | 8.74          |
| polka                    | 0.5.2   | ✓      | 47885.6    | 20.39        | 8.54          |
| foxify                   | 0.10.20 | ✓      | 47883.2    | 20.39        | 7.85          |
| fastify                  | 4.10.2  | ✓      | 47521.6    | 20.55        | 8.52          |
| connect                  | 3.7.0   | ✗      | 47176.8    | 20.70        | 8.41          |
| 0http                    | 3.4.2   | ✓      | 46386.4    | 21.06        | 8.27          |
| server-base              | 7.1.32  | ✗      | 45974.4    | 21.26        | 8.20          |
| server-base-router       | 7.1.32  | ✓      | 45913.6    | 21.28        | 8.19          |
| h3                       | 0.8.6   | ✗      | 45854.6    | 21.32        | 7.52          |
| yeps                     | 1.1.1   | ✗      | 45478.4    | 21.49        | 8.11          |
| h3-router                | 0.8.6   | ✓      | 44850.4    | 21.81        | 7.36          |
| connect-router           | 1.3.7   | ✓      | 43997.6    | 22.23        | 7.85          |
| micro-route              | 2.5.0   | ✓      | 43976.8    | 22.24        | 7.84          |
| restana                  | 4.9.7   | ✓      | 43897.6    | 22.29        | 7.83          |
| trek-engine              | 1.0.5   | ✗      | 42031.0    | 23.31        | 6.89          |
| trek-router              | 1.2.0   | ✓      | 39899.0    | 24.57        | 6.54          |
| vapr                     | 0.6.0   | ✓      | 37480.0    | 26.19        | 6.15          |
| yeps-router              | 1.2.0   | ✓      | 36459.0    | 26.93        | 6.50          |
| koa                      | 2.14.1  | ✗      | 35808.2    | 27.43        | 6.39          |
| spirit                   | 0.6.1   | ✗      | 35688.2    | 27.54        | 6.36          |
| spirit-router            | 0.5.0   | ✓      | 34858.4    | 28.21        | 6.22          |
| take-five                | 2.0.0   | ✓      | 34578.6    | 28.42        | 12.43         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 34047.6    | 28.88        | 6.07          |
| total.js                 | 3.4.13  | ✓      | 33894.4    | 29.00        | 10.38         |
| restify                  | 8.6.1   | ✓      | 32413.8    | 30.34        | 5.84          |
| koa-router               | 12.0.0  | ✓      | 29486.4    | 33.42        | 5.26          |
| hapi                     | 20.2.2  | ✓      | 26246.0    | 37.61        | 4.68          |
| microrouter              | 3.1.3   | ✓      | 25715.2    | 38.39        | 4.59          |
| trpc-router              | 9.27.3  | ✓      | 22542.8    | 43.85        | 4.99          |
| egg.js                   | 3.9.1   | ✓      | 13021.8    | 76.28        | 4.66          |
| express                  | 4.18.2  | ✓      | 10595.3    | 93.83        | 1.89          |
| express-with-middlewares | 4.18.2  | ✓      | 9337.9     | 106.50       | 3.47          |
| express-route-prefix     | 4.18.2  | ✓      | 9018.6     | 110.31       | 3.34          |
| fastify-big-json         | 4.10.2  | ✓      | 8598.8     | 115.85       | 98.93         |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Nov 07 2022 03:00:19 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 28962.8    | 34.18        | 5.17          |
| h3                       | 0.8.6   | ✗      | 28938.8    | 34.19        | 4.75          |
| micro                    | 9.4.1   | ✗      | 28892.8    | 34.22        | 5.15          |
| h3-router                | 0.8.6   | ✓      | 28874.4    | 34.29        | 4.74          |
| spirit-router            | 0.5.0   | ✓      | 28329.6    | 34.98        | 5.05          |
| polkadot                 | 1.0.0   | ✗      | 28083.6    | 35.21        | 5.01          |
| foxify                   | 0.10.20 | ✓      | 28044.4    | 35.29        | 4.60          |
| fastify                  | 4.9.2   | ✓      | 27830.8    | 35.48        | 4.99          |
| polka                    | 0.5.2   | ✓      | 27358.4    | 36.11        | 4.88          |
| 0http                    | 3.4.1   | ✓      | 26883.6    | 36.74        | 4.79          |
| connect                  | 3.7.0   | ✗      | 26854.9    | 36.86        | 4.79          |
| spirit                   | 0.6.1   | ✗      | 26075.1    | 37.97        | 4.65          |
| rayo                     | 1.3.10  | ✓      | 26004.0    | 37.98        | 4.64          |
| server-base              | 7.1.32  | ✗      | 25903.2    | 38.13        | 4.62          |
| server-base-router       | 7.1.32  | ✓      | 25897.6    | 38.15        | 4.62          |
| yeps                     | 1.1.1   | ✗      | 25787.2    | 38.31        | 4.60          |
| connect-router           | 1.3.7   | ✓      | 24928.0    | 39.63        | 4.45          |
| trek-engine              | 1.0.5   | ✗      | 23769.2    | 41.58        | 3.90          |
| yeps-router              | 1.2.0   | ✓      | 22812.0    | 43.33        | 4.07          |
| micro-route              | 2.5.0   | ✓      | 22709.2    | 43.53        | 4.05          |
| trek-router              | 1.2.0   | ✓      | 21955.5    | 45.06        | 3.60          |
| koa                      | 2.13.4  | ✗      | 21903.9    | 45.14        | 3.91          |
| vapr                     | 0.6.0   | ✓      | 21795.2    | 45.38        | 3.58          |
| restana                  | 4.9.6   | ✓      | 21210.4    | 46.65        | 3.78          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20591.2    | 48.07        | 3.67          |
| restify                  | 8.6.1   | ✓      | 20270.7    | 48.82        | 3.65          |
| take-five                | 2.0.0   | ✓      | 19062.1    | 51.95        | 6.85          |
| koa-router               | 12.0.0  | ✓      | 18854.7    | 52.52        | 3.36          |
| total.js                 | 3.4.13  | ✓      | 18641.5    | 53.14        | 5.71          |
| hapi                     | 20.2.2  | ✓      | 18598.1    | 53.24        | 3.32          |
| trpc-router              | 9.27.4  | ✓      | 16913.6    | 58.60        | 3.74          |
| microrouter              | 3.1.3   | ✓      | 16464.3    | 60.22        | 2.94          |
| egg.js                   | 3.3.3   | ✓      | 10242.4    | 97.07        | 3.66          |
| fastify-big-json         | 4.9.2   | ✓      | 7395.5     | 134.66       | 85.09         |
| express                  | 4.18.2  | ✓      | 6725.2     | 147.99       | 1.20          |
| express-route-prefix     | 4.18.2  | ✓      | 6413.4     | 155.23       | 2.37          |
| express-with-middlewares | 4.18.2  | ✓      | 5970.8     | 166.69       | 2.22          |

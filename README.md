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
* __Run:__ Mon Dec 26 2022 02:30:44 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 62086.2    | 15.60        | 11.07         |
| 0http                    | 3.4.2   | ✓      | 61168.0    | 15.87        | 10.91         |
| bare                     | 10.13.0 | ✗      | 60920.8    | 15.92        | 10.87         |
| polka                    | 0.5.2   | ✓      | 60791.2    | 15.95        | 10.84         |
| h3                       | 0.8.6   | ✗      | 59636.8    | 16.27        | 9.78          |
| fastify                  | 4.10.2  | ✓      | 59262.4    | 16.38        | 10.62         |
| foxify                   | 0.10.20 | ✓      | 59227.2    | 16.39        | 9.72          |
| h3-router                | 0.8.6   | ✓      | 59028.0    | 16.44        | 9.68          |
| connect                  | 3.7.0   | ✗      | 57083.8    | 17.02        | 10.18         |
| micro                    | 9.4.1   | ✗      | 56932.0    | 17.08        | 10.15         |
| server-base              | 7.1.32  | ✗      | 56644.0    | 17.15        | 10.10         |
| server-base-router       | 7.1.32  | ✓      | 56532.8    | 17.19        | 10.08         |
| restana                  | 4.9.7   | ✓      | 56245.6    | 17.29        | 10.03         |
| yeps                     | 1.1.1   | ✗      | 54178.4    | 17.95        | 9.66          |
| micro-route              | 2.5.0   | ✓      | 51968.0    | 18.75        | 9.27          |
| connect-router           | 1.3.7   | ✓      | 51695.2    | 18.85        | 9.22          |
| trek-router              | 1.2.0   | ✓      | 49752.2    | 19.60        | 8.16          |
| trek-engine              | 1.0.5   | ✗      | 49440.8    | 19.74        | 8.11          |
| vapr                     | 0.6.0   | ✓      | 48893.6    | 19.96        | 8.02          |
| yeps-router              | 1.2.0   | ✓      | 45495.2    | 21.49        | 8.11          |
| spirit                   | 0.6.1   | ✗      | 45150.4    | 21.64        | 8.05          |
| koa                      | 2.14.1  | ✗      | 44287.8    | 22.09        | 7.90          |
| spirit-router            | 0.5.0   | ✓      | 43612.0    | 22.43        | 7.78          |
| take-five                | 2.0.0   | ✓      | 42091.2    | 23.25        | 15.13         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41876.0    | 23.40        | 7.47          |
| total.js                 | 3.4.13  | ✓      | 40900.0    | 23.94        | 12.52         |
| restify                  | 8.6.1   | ✓      | 39209.0    | 25.01        | 7.07          |
| koa-router               | 12.0.0  | ✓      | 38400.0    | 25.55        | 6.85          |
| hapi                     | 20.2.2  | ✓      | 34248.6    | 28.73        | 6.11          |
| microrouter              | 3.1.3   | ✓      | 32722.8    | 30.06        | 5.84          |
| trpc-router              | 9.27.3  | ✓      | 28608.8    | 34.45        | 6.33          |
| egg.js                   | 3.9.2   | ✓      | 16996.5    | 58.29        | 6.08          |
| express                  | 4.18.2  | ✓      | 13926.0    | 71.29        | 2.48          |
| express-with-middlewares | 4.18.2  | ✓      | 12394.0    | 80.18        | 4.61          |
| express-route-prefix     | 4.18.2  | ✓      | 12112.0    | 82.02        | 4.48          |
| fastify-big-json         | 4.10.2  | ✓      | 11594.2    | 85.78        | 133.41        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

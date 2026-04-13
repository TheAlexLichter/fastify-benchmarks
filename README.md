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
* __Run:__ Mon Apr 13 2026 04:33:43 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 71913.2    | 13.42        | 12.83         |
| 0http                    | 3.5.3   | ✓      | 67599.2    | 14.30        | 12.05         |
| restana                  | 4.9.9   | ✓      | 62717.6    | 15.43        | 11.18         |
| h3                       | 0.8.6   | ✗      | 62700.0    | 15.46        | 10.29         |
| bare                     | 10.13.0 | ✗      | 61473.6    | 15.77        | 10.96         |
| h3-router                | 0.8.6   | ✓      | 61120.8    | 15.88        | 10.03         |
| foxify                   | 0.10.20 | ✓      | 60723.2    | 15.97        | 9.96          |
| polka                    | 0.5.2   | ✓      | 59477.6    | 16.31        | 10.61         |
| connect                  | 3.7.0   | ✗      | 58767.2    | 16.53        | 10.48         |
| micro                    | 9.4.1   | ✗      | 58319.2    | 16.65        | 10.40         |
| fastify                  | 4.29.1  | ✓      | 57342.4    | 16.94        | 10.28         |
| server-base              | 7.1.32  | ✗      | 56054.4    | 17.34        | 10.00         |
| server-base-router       | 7.1.32  | ✓      | 54844.0    | 17.73        | 9.78          |
| yeps                     | 1.1.1   | ✗      | 54150.4    | 17.97        | 9.66          |
| connect-router           | 1.3.8   | ✓      | 51888.8    | 18.78        | 9.25          |
| micro-route              | 2.5.0   | ✓      | 51669.6    | 18.85        | 9.21          |
| trek-engine              | 1.0.5   | ✗      | 49488.0    | 19.71        | 8.12          |
| trek-router              | 1.2.0   | ✓      | 47945.6    | 20.36        | 7.86          |
| vapr                     | 0.6.0   | ✓      | 46322.4    | 21.09        | 7.60          |
| spirit-router            | 0.5.0   | ✓      | 45507.2    | 21.50        | 8.12          |
| spirit                   | 0.6.1   | ✗      | 45088.0    | 21.72        | 8.04          |
| yeps-router              | 1.2.0   | ✓      | 44760.0    | 21.85        | 7.98          |
| koa                      | 2.16.4  | ✗      | 42753.6    | 22.90        | 7.62          |
| total.js                 | 3.4.13  | ✓      | 40328.8    | 24.29        | 12.34         |
| take-five                | 2.0.0   | ✓      | 39945.8    | 24.53        | 14.36         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39923.8    | 24.56        | 7.12          |
| restify                  | 8.6.1   | ✓      | 39379.4    | 24.89        | 7.10          |
| koa-router               | 12.0.1  | ✓      | 37119.4    | 26.43        | 6.62          |
| microrouter              | 3.1.3   | ✓      | 33028.2    | 29.77        | 5.89          |
| hapi                     | 20.3.0  | ✓      | 32974.8    | 29.82        | 5.88          |
| trpc-router              | 9.27.4  | ✓      | 26830.4    | 36.77        | 5.94          |
| egg.js                   | 3.34.0  | ✓      | 17568.9    | 56.40        | 6.28          |
| express                  | 4.22.1  | ✓      | 13030.0    | 76.20        | 2.32          |
| express-with-middlewares | 4.22.1  | ✓      | 12535.6    | 79.21        | 4.66          |
| fastify-big-json         | 4.29.1  | ✓      | 12437.2    | 79.85        | 143.08        |
| express-route-prefix     | 4.22.1  | ✓      | 10324.9    | 96.27        | 3.82          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

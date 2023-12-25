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
* __Run:__ Mon Dec 25 2023 02:11:25 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 64113.6    | 15.09        | 11.43         |
| 0http                    | 3.5.2   | ✓      | 62874.4    | 15.41        | 11.21         |
| h3-router                | 0.8.6   | ✓      | 60704.0    | 15.98        | 9.96          |
| bare                     | 10.13.0 | ✗      | 59888.8    | 16.20        | 10.68         |
| h3                       | 0.8.6   | ✗      | 59764.0    | 16.24        | 9.80          |
| foxify                   | 0.10.20 | ✓      | 58531.2    | 16.58        | 9.60          |
| connect                  | 3.7.0   | ✗      | 57020.8    | 17.04        | 10.17         |
| fastify                  | 4.25.2  | ✓      | 56084.0    | 17.34        | 10.06         |
| polka                    | 0.5.2   | ✓      | 55588.8    | 17.49        | 9.91          |
| micro                    | 9.4.1   | ✗      | 53696.0    | 18.13        | 9.58          |
| server-base-router       | 7.1.32  | ✓      | 53642.4    | 18.14        | 9.57          |
| restana                  | 4.9.7   | ✓      | 53600.8    | 18.16        | 9.56          |
| server-base              | 7.1.32  | ✗      | 53085.6    | 18.34        | 9.47          |
| yeps                     | 1.1.1   | ✗      | 52396.8    | 18.59        | 9.34          |
| micro-route              | 2.5.0   | ✓      | 48424.8    | 20.16        | 8.64          |
| connect-router           | 1.3.8   | ✓      | 48033.6    | 20.32        | 8.57          |
| trek-engine              | 1.0.5   | ✗      | 46866.6    | 20.84        | 7.69          |
| trek-router              | 1.2.0   | ✓      | 46211.2    | 21.15        | 7.58          |
| vapr                     | 0.6.0   | ✓      | 44892.0    | 21.78        | 7.36          |
| yeps-router              | 1.2.0   | ✓      | 42952.8    | 22.78        | 7.66          |
| koa                      | 2.14.2  | ✗      | 41199.2    | 23.77        | 7.35          |
| spirit                   | 0.6.1   | ✗      | 40536.8    | 24.18        | 7.23          |
| spirit-router            | 0.5.0   | ✓      | 39648.0    | 24.72        | 7.07          |
| total.js                 | 3.4.13  | ✓      | 38962.6    | 25.17        | 11.93         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38469.0    | 25.48        | 6.86          |
| take-five                | 2.0.0   | ✓      | 38087.4    | 25.75        | 13.69         |
| restify                  | 8.6.1   | ✓      | 37203.4    | 26.38        | 6.71          |
| koa-router               | 12.0.1  | ✓      | 36295.4    | 27.05        | 6.47          |
| hapi                     | 20.3.0  | ✓      | 32405.8    | 30.36        | 5.78          |
| microrouter              | 3.1.3   | ✓      | 31976.4    | 30.77        | 5.70          |
| trpc-router              | 9.27.4  | ✓      | 26482.8    | 37.26        | 5.86          |
| egg.js                   | 3.17.5  | ✓      | 17430.6    | 56.85        | 6.23          |
| express                  | 4.18.2  | ✓      | 13569.4    | 73.14        | 2.42          |
| express-with-middlewares | 4.18.2  | ✓      | 12590.4    | 78.86        | 4.68          |
| fastify-big-json         | 4.25.2  | ✓      | 12493.2    | 79.48        | 143.74        |
| express-route-prefix     | 4.18.2  | ✓      | 10921.8    | 90.98        | 4.04          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

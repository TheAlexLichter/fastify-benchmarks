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
* __Run:__ Mon Jun 10 2024 02:23:59 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 70100.4    | 13.77        | 12.50         |
| polkadot                 | 1.0.0   | ✗      | 66390.8    | 14.57        | 11.84         |
| h3                       | 0.8.6   | ✗      | 64174.8    | 15.08        | 10.53         |
| bare                     | 10.13.0 | ✗      | 61178.4    | 15.85        | 10.91         |
| restana                  | 4.9.9   | ✓      | 60816.8    | 15.95        | 10.85         |
| h3-router                | 0.8.6   | ✓      | 59285.6    | 16.37        | 9.73          |
| foxify                   | 0.10.20 | ✓      | 59271.2    | 16.37        | 9.72          |
| connect                  | 3.7.0   | ✗      | 58811.2    | 16.51        | 10.49         |
| polka                    | 0.5.2   | ✓      | 58316.0    | 16.66        | 10.40         |
| micro                    | 9.4.1   | ✗      | 57412.8    | 16.93        | 10.24         |
| fastify                  | 4.27.0  | ✓      | 56226.4    | 17.29        | 10.08         |
| server-base              | 7.1.32  | ✗      | 54516.0    | 17.85        | 9.72          |
| yeps                     | 1.1.1   | ✗      | 54401.6    | 17.89        | 9.70          |
| server-base-router       | 7.1.32  | ✓      | 53258.4    | 18.28        | 9.50          |
| connect-router           | 1.3.8   | ✓      | 51008.8    | 19.11        | 9.10          |
| micro-route              | 2.5.0   | ✓      | 50566.4    | 19.28        | 9.02          |
| trek-engine              | 1.0.5   | ✗      | 47898.4    | 20.38        | 7.86          |
| trek-router              | 1.2.0   | ✓      | 47330.4    | 20.63        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 45459.2    | 21.49        | 7.46          |
| spirit                   | 0.6.1   | ✗      | 44163.2    | 22.16        | 7.88          |
| yeps-router              | 1.2.0   | ✓      | 43900.8    | 22.27        | 7.83          |
| koa                      | 2.15.3  | ✗      | 43627.2    | 22.43        | 7.78          |
| spirit-router            | 0.5.0   | ✓      | 43209.6    | 22.63        | 7.71          |
| total.js                 | 3.4.13  | ✓      | 39996.8    | 24.50        | 12.24         |
| take-five                | 2.0.0   | ✓      | 39511.0    | 24.82        | 14.21         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39349.8    | 24.91        | 7.02          |
| restify                  | 8.6.1   | ✓      | 39032.6    | 25.13        | 7.04          |
| koa-router               | 12.0.1  | ✓      | 37947.0    | 25.86        | 6.77          |
| hapi                     | 20.3.0  | ✓      | 34021.2    | 28.89        | 6.07          |
| microrouter              | 3.1.3   | ✓      | 32262.6    | 30.48        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 26242.4    | 37.60        | 5.81          |
| egg.js                   | 3.24.1  | ✓      | 17743.6    | 55.82        | 6.35          |
| express                  | 4.19.2  | ✓      | 13498.8    | 73.53        | 2.41          |
| fastify-big-json         | 4.27.0  | ✓      | 12972.6    | 76.55        | 149.26        |
| express-with-middlewares | 4.19.2  | ✓      | 12485.6    | 79.54        | 4.64          |
| express-route-prefix     | 4.19.2  | ✓      | 10958.0    | 90.67        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

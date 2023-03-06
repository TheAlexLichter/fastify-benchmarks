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
* __Run:__ Mon Mar 06 2023 02:41:58 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 62130.4    | 15.59        | 11.08         |
| bare                     | 10.13.0 | ✗      | 61435.2    | 15.78        | 10.96         |
| 0http                    | 3.5.1   | ✓      | 60807.2    | 15.97        | 10.84         |
| h3                       | 0.8.6   | ✗      | 59965.6    | 16.19        | 9.84          |
| polka                    | 0.5.2   | ✓      | 59064.8    | 16.43        | 10.53         |
| h3-router                | 0.8.6   | ✓      | 58523.2    | 16.60        | 9.60          |
| foxify                   | 0.10.20 | ✓      | 58245.6    | 16.67        | 9.55          |
| micro                    | 9.4.1   | ✗      | 57833.6    | 16.79        | 10.31         |
| connect                  | 3.7.0   | ✗      | 57064.0    | 17.03        | 10.18         |
| fastify                  | 4.14.0  | ✓      | 56761.6    | 17.12        | 10.18         |
| server-base-router       | 7.1.32  | ✓      | 55440.0    | 17.54        | 9.89          |
| restana                  | 4.9.7   | ✓      | 55203.2    | 17.58        | 9.84          |
| server-base              | 7.1.32  | ✗      | 54686.4    | 17.78        | 9.75          |
| yeps                     | 1.1.1   | ✗      | 54232.0    | 17.94        | 9.67          |
| connect-router           | 1.3.8   | ✓      | 52296.0    | 18.63        | 9.33          |
| micro-route              | 2.5.0   | ✓      | 52066.4    | 18.71        | 9.29          |
| trek-router              | 1.2.0   | ✓      | 49413.6    | 19.74        | 8.11          |
| trek-engine              | 1.0.5   | ✗      | 48965.0    | 19.93        | 8.03          |
| vapr                     | 0.6.0   | ✓      | 48481.6    | 20.14        | 7.95          |
| spirit                   | 0.6.1   | ✗      | 44255.2    | 22.11        | 7.89          |
| koa                      | 2.14.1  | ✗      | 44192.0    | 22.13        | 7.88          |
| yeps-router              | 1.2.0   | ✓      | 43624.8    | 22.42        | 7.78          |
| take-five                | 2.0.0   | ✓      | 41505.6    | 23.59        | 14.92         |
| spirit-router            | 0.5.0   | ✓      | 41281.6    | 23.74        | 7.36          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40977.6    | 23.91        | 7.31          |
| total.js                 | 3.4.13  | ✓      | 40729.6    | 24.05        | 12.47         |
| restify                  | 8.6.1   | ✓      | 39368.0    | 24.90        | 7.10          |
| koa-router               | 12.0.0  | ✓      | 37655.4    | 26.07        | 6.72          |
| hapi                     | 20.3.0  | ✓      | 33846.8    | 29.04        | 6.04          |
| microrouter              | 3.1.3   | ✓      | 32190.4    | 30.57        | 5.74          |
| trpc-router              | 9.27.3  | ✓      | 28064.8    | 35.13        | 6.21          |
| egg.js                   | 3.15.0  | ✓      | 16485.2    | 60.14        | 5.90          |
| express                  | 4.18.2  | ✓      | 13732.6    | 72.30        | 2.45          |
| express-route-prefix     | 4.18.2  | ✓      | 12002.5    | 82.78        | 4.44          |
| express-with-middlewares | 4.18.2  | ✓      | 11855.0    | 83.77        | 4.41          |
| fastify-big-json         | 4.14.0  | ✓      | 11704.2    | 84.99        | 134.67        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

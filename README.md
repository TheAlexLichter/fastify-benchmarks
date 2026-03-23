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
* __Run:__ Mon Mar 23 2026 04:05:30 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66243.6    | 14.61        | 11.81         |
| polkadot                 | 1.0.0   | ✗      | 64386.4    | 15.03        | 11.48         |
| h3-router                | 0.8.6   | ✓      | 61239.2    | 15.84        | 10.04         |
| h3                       | 0.8.6   | ✗      | 60807.2    | 15.97        | 9.97          |
| restana                  | 4.9.9   | ✓      | 60371.2    | 16.09        | 10.77         |
| bare                     | 10.13.0 | ✗      | 59432.8    | 16.32        | 10.60         |
| foxify                   | 0.10.20 | ✓      | 58828.8    | 16.50        | 9.65          |
| connect                  | 3.7.0   | ✗      | 57365.6    | 16.93        | 10.23         |
| polka                    | 0.5.2   | ✓      | 57360.0    | 16.93        | 10.23         |
| micro                    | 9.4.1   | ✗      | 55937.6    | 17.38        | 9.97          |
| fastify                  | 4.29.1  | ✓      | 55528.8    | 17.51        | 9.96          |
| server-base              | 7.1.32  | ✗      | 55405.6    | 17.55        | 9.88          |
| server-base-router       | 7.1.32  | ✓      | 54436.8    | 17.87        | 9.71          |
| yeps                     | 1.1.1   | ✗      | 52084.8    | 18.70        | 9.29          |
| connect-router           | 1.3.8   | ✓      | 50108.0    | 19.46        | 8.94          |
| micro-route              | 2.5.0   | ✓      | 49312.8    | 19.78        | 8.79          |
| trek-engine              | 1.0.5   | ✗      | 48628.0    | 20.07        | 7.98          |
| trek-router              | 1.2.0   | ✓      | 47700.0    | 20.46        | 7.82          |
| vapr                     | 0.6.0   | ✓      | 46790.4    | 20.88        | 7.67          |
| spirit                   | 0.6.1   | ✗      | 43750.4    | 22.32        | 7.80          |
| yeps-router              | 1.2.0   | ✓      | 43386.4    | 22.55        | 7.74          |
| koa                      | 2.16.4  | ✗      | 41301.6    | 23.71        | 7.37          |
| spirit-router            | 0.5.0   | ✓      | 41190.4    | 23.80        | 7.35          |
| total.js                 | 3.4.13  | ✓      | 39319.4    | 24.93        | 12.04         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38848.2    | 25.25        | 6.93          |
| take-five                | 2.0.0   | ✓      | 38508.2    | 25.47        | 13.84         |
| restify                  | 8.6.1   | ✓      | 38203.0    | 25.68        | 6.89          |
| koa-router               | 12.0.1  | ✓      | 36012.2    | 27.26        | 6.42          |
| hapi                     | 20.3.0  | ✓      | 31940.4    | 30.81        | 5.70          |
| microrouter              | 3.1.3   | ✓      | 31675.2    | 31.08        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 26652.4    | 37.02        | 5.90          |
| egg.js                   | 3.34.0  | ✓      | 16914.2    | 58.59        | 6.05          |
| express                  | 4.22.1  | ✓      | 13668.0    | 72.63        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12577.6    | 78.96        | 144.73        |
| express-with-middlewares | 4.22.1  | ✓      | 12410.4    | 80.02        | 4.62          |
| express-route-prefix     | 4.22.1  | ✓      | 10572.2    | 94.02        | 3.91          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

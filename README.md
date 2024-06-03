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
* __Run:__ Mon Jun 03 2024 02:15:52 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67765.6    | 14.26        | 12.09         |
| 0http                    | 3.5.3   | ✓      | 67337.2    | 14.36        | 12.01         |
| h3                       | 0.8.6   | ✗      | 66070.0    | 14.63        | 10.84         |
| h3-router                | 0.8.6   | ✓      | 64578.4    | 14.98        | 10.59         |
| restana                  | 4.9.9   | ✓      | 60004.8    | 16.17        | 10.70         |
| foxify                   | 0.10.20 | ✓      | 58092.8    | 16.72        | 9.53          |
| bare                     | 10.13.0 | ✗      | 57833.6    | 16.80        | 10.31         |
| polka                    | 0.5.2   | ✓      | 57196.8    | 16.99        | 10.20         |
| micro                    | 9.4.1   | ✗      | 55567.2    | 17.50        | 9.91          |
| fastify                  | 4.27.0  | ✓      | 55258.4    | 17.61        | 9.91          |
| connect                  | 3.7.0   | ✗      | 55242.4    | 17.60        | 9.85          |
| server-base-router       | 7.1.32  | ✓      | 54222.4    | 17.95        | 9.67          |
| server-base              | 7.1.32  | ✗      | 52540.0    | 18.53        | 9.37          |
| yeps                     | 1.1.1   | ✗      | 52197.6    | 18.66        | 9.31          |
| connect-router           | 1.3.8   | ✓      | 48733.6    | 20.03        | 8.69          |
| trek-engine              | 1.0.5   | ✗      | 48565.6    | 20.09        | 7.97          |
| micro-route              | 2.5.0   | ✓      | 48412.8    | 20.15        | 8.63          |
| trek-router              | 1.2.0   | ✓      | 48364.8    | 20.19        | 7.93          |
| vapr                     | 0.6.0   | ✓      | 45596.8    | 21.42        | 7.48          |
| yeps-router              | 1.2.0   | ✓      | 43924.0    | 22.26        | 7.83          |
| spirit                   | 0.6.1   | ✗      | 43700.8    | 22.38        | 7.79          |
| koa                      | 2.15.3  | ✗      | 42624.0    | 22.96        | 7.60          |
| spirit-router            | 0.5.0   | ✓      | 42118.4    | 23.27        | 7.51          |
| total.js                 | 3.4.13  | ✓      | 39813.8    | 24.62        | 12.19         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39546.2    | 24.79        | 7.05          |
| restify                  | 8.6.1   | ✓      | 39257.0    | 24.97        | 7.08          |
| take-five                | 2.0.0   | ✓      | 39139.8    | 25.06        | 14.07         |
| koa-router               | 12.0.1  | ✓      | 36867.8    | 26.63        | 6.57          |
| hapi                     | 20.3.0  | ✓      | 33036.2    | 29.77        | 5.89          |
| microrouter              | 3.1.3   | ✓      | 31559.0    | 31.19        | 5.63          |
| trpc-router              | 9.27.4  | ✓      | 26014.0    | 37.93        | 5.76          |
| egg.js                   | 3.23.0  | ✓      | 17189.5    | 57.65        | 6.15          |
| express                  | 4.19.2  | ✓      | 13526.2    | 73.37        | 2.41          |
| fastify-big-json         | 4.27.0  | ✓      | 12751.4    | 77.89        | 146.72        |
| express-with-middlewares | 4.19.2  | ✓      | 12703.0    | 78.17        | 4.72          |
| express-route-prefix     | 4.19.2  | ✓      | 10811.8    | 91.93        | 4.00          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

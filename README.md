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
* __Run:__ Mon Nov 17 2025 02:56:03 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68153.6    | 14.18        | 12.16         |
| 0http                    | 3.5.3   | ✓      | 66203.2    | 14.61        | 11.81         |
| h3-router                | 0.8.6   | ✓      | 66075.6    | 14.63        | 10.84         |
| h3                       | 0.8.6   | ✗      | 62542.4    | 15.50        | 10.26         |
| restana                  | 4.9.9   | ✓      | 61252.8    | 15.85        | 10.92         |
| foxify                   | 0.10.20 | ✓      | 60694.4    | 15.98        | 9.96          |
| bare                     | 10.13.0 | ✗      | 58556.0    | 16.58        | 10.44         |
| polka                    | 0.5.2   | ✓      | 56430.4    | 17.22        | 10.06         |
| fastify                  | 4.29.1  | ✓      | 56335.2    | 17.26        | 10.10         |
| micro                    | 9.4.1   | ✗      | 56265.6    | 17.28        | 10.03         |
| connect                  | 3.7.0   | ✗      | 54195.2    | 17.95        | 9.66          |
| server-base-router       | 7.1.32  | ✓      | 53140.0    | 18.32        | 9.48          |
| server-base              | 7.1.32  | ✗      | 53065.6    | 18.35        | 9.46          |
| yeps                     | 1.1.1   | ✗      | 51836.0    | 18.79        | 9.24          |
| micro-route              | 2.5.0   | ✓      | 49793.6    | 19.59        | 8.88          |
| connect-router           | 1.3.8   | ✓      | 49354.4    | 19.77        | 8.80          |
| trek-engine              | 1.0.5   | ✗      | 46137.6    | 21.17        | 7.57          |
| trek-router              | 1.2.0   | ✓      | 45656.8    | 21.41        | 7.49          |
| vapr                     | 0.6.0   | ✓      | 44170.4    | 22.14        | 7.25          |
| yeps-router              | 1.2.0   | ✓      | 42924.0    | 22.80        | 7.65          |
| koa                      | 2.16.3  | ✗      | 42491.2    | 23.04        | 7.58          |
| spirit-router            | 0.5.0   | ✓      | 40172.0    | 24.38        | 7.16          |
| spirit                   | 0.6.1   | ✗      | 39796.0    | 24.63        | 7.10          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39189.8    | 25.02        | 6.99          |
| restify                  | 8.6.1   | ✓      | 38649.4    | 25.38        | 6.97          |
| total.js                 | 3.4.13  | ✓      | 38599.2    | 25.40        | 11.82         |
| take-five                | 2.0.0   | ✓      | 37213.8    | 26.37        | 13.38         |
| koa-router               | 12.0.1  | ✓      | 36123.4    | 27.19        | 6.44          |
| hapi                     | 20.3.0  | ✓      | 33636.2    | 29.23        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 31426.4    | 31.31        | 5.60          |
| trpc-router              | 9.27.4  | ✓      | 26162.8    | 37.70        | 5.79          |
| egg.js                   | 3.31.0  | ✓      | 17221.1    | 57.54        | 6.16          |
| express                  | 4.21.2  | ✓      | 13685.6    | 72.52        | 2.44          |
| fastify-big-json         | 4.29.1  | ✓      | 12579.0    | 78.95        | 144.72        |
| express-with-middlewares | 4.21.2  | ✓      | 12375.4    | 80.24        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 10923.0    | 90.97        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

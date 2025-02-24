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
* __Run:__ Mon Feb 24 2025 02:41:55 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 64523.2    | 15.00        | 11.51         |
| polkadot                 | 1.0.0   | ✗      | 62946.8    | 15.40        | 11.23         |
| h3-router                | 0.8.6   | ✓      | 58932.0    | 16.47        | 9.67          |
| bare                     | 10.13.0 | ✗      | 58287.2    | 16.66        | 10.39         |
| h3                       | 0.8.6   | ✗      | 57753.6    | 16.82        | 9.47          |
| foxify                   | 0.10.20 | ✓      | 56809.6    | 17.11        | 9.32          |
| restana                  | 4.9.9   | ✓      | 54819.2    | 17.76        | 9.78          |
| fastify                  | 4.29.0  | ✓      | 54665.6    | 17.80        | 9.80          |
| polka                    | 0.5.2   | ✓      | 54628.0    | 17.81        | 9.74          |
| micro                    | 9.4.1   | ✗      | 54004.8    | 18.02        | 9.63          |
| connect                  | 3.7.0   | ✗      | 53858.4    | 18.07        | 9.61          |
| server-base              | 7.1.32  | ✗      | 53796.8    | 18.09        | 9.59          |
| server-base-router       | 7.1.32  | ✓      | 53192.8    | 18.30        | 9.49          |
| yeps                     | 1.1.1   | ✗      | 51644.8    | 18.87        | 9.21          |
| connect-router           | 1.3.8   | ✓      | 48812.8    | 19.99        | 8.71          |
| micro-route              | 2.5.0   | ✓      | 48615.2    | 20.07        | 8.67          |
| trek-engine              | 1.0.5   | ✗      | 47184.0    | 20.70        | 7.74          |
| trek-router              | 1.2.0   | ✓      | 47182.4    | 20.70        | 7.74          |
| vapr                     | 0.6.0   | ✓      | 45355.2    | 21.55        | 7.44          |
| yeps-router              | 1.2.0   | ✓      | 42997.4    | 22.76        | 7.67          |
| spirit                   | 0.6.1   | ✗      | 41204.8    | 23.77        | 7.35          |
| koa                      | 2.15.4  | ✗      | 40950.6    | 23.91        | 7.30          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39682.2    | 24.70        | 7.08          |
| spirit-router            | 0.5.0   | ✓      | 39666.4    | 24.71        | 7.07          |
| total.js                 | 3.4.13  | ✓      | 38931.8    | 25.19        | 11.92         |
| take-five                | 2.0.0   | ✓      | 37949.8    | 25.85        | 13.64         |
| restify                  | 8.6.1   | ✓      | 37869.8    | 25.91        | 6.83          |
| koa-router               | 12.0.1  | ✓      | 35981.4    | 27.29        | 6.42          |
| hapi                     | 20.3.0  | ✓      | 32648.6    | 30.12        | 5.82          |
| microrouter              | 3.1.3   | ✓      | 30672.0    | 32.11        | 5.47          |
| trpc-router              | 9.27.4  | ✓      | 26962.8    | 36.58        | 5.97          |
| egg.js                   | 3.30.1  | ✓      | 16426.9    | 60.34        | 5.87          |
| express                  | 4.21.2  | ✓      | 13446.2    | 73.84        | 2.40          |
| fastify-big-json         | 4.29.0  | ✓      | 12443.6    | 79.81        | 143.17        |
| express-with-middlewares | 4.21.2  | ✓      | 12202.6    | 81.37        | 4.54          |
| express-route-prefix     | 4.21.2  | ✓      | 10626.6    | 93.54        | 3.93          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

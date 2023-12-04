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
* __Run:__ Mon Dec 04 2023 02:12:12 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 64583.6    | 14.99        | 11.52         |
| h3                       | 0.8.6   | ✗      | 61874.4    | 15.66        | 10.15         |
| 0http                    | 3.5.2   | ✓      | 61798.4    | 15.68        | 11.02         |
| h3-router                | 0.8.6   | ✓      | 59943.2    | 16.19        | 9.83          |
| bare                     | 10.13.0 | ✗      | 58246.4    | 16.67        | 10.39         |
| polka                    | 0.5.2   | ✓      | 57384.0    | 16.93        | 10.23         |
| foxify                   | 0.10.20 | ✓      | 56536.0    | 17.19        | 9.27          |
| fastify                  | 4.24.3  | ✓      | 54774.4    | 17.76        | 9.82          |
| connect                  | 3.7.0   | ✗      | 54772.0    | 17.76        | 9.77          |
| micro                    | 9.4.1   | ✗      | 53702.4    | 18.12        | 9.58          |
| server-base              | 7.1.32  | ✗      | 53494.4    | 18.19        | 9.54          |
| restana                  | 4.9.7   | ✓      | 52281.6    | 18.63        | 9.32          |
| server-base-router       | 7.1.32  | ✓      | 51256.8    | 19.01        | 9.14          |
| yeps                     | 1.1.1   | ✗      | 51005.6    | 19.11        | 9.10          |
| connect-router           | 1.3.8   | ✓      | 49281.6    | 19.79        | 8.79          |
| micro-route              | 2.5.0   | ✓      | 48795.2    | 20.00        | 8.70          |
| trek-router              | 1.2.0   | ✓      | 46765.6    | 20.89        | 7.67          |
| trek-engine              | 1.0.5   | ✗      | 46469.6    | 21.02        | 7.62          |
| vapr                     | 0.6.0   | ✓      | 44228.8    | 22.11        | 7.25          |
| spirit                   | 0.6.1   | ✗      | 41840.8    | 23.40        | 7.46          |
| yeps-router              | 1.2.0   | ✓      | 41683.2    | 23.49        | 7.43          |
| koa                      | 2.14.2  | ✗      | 41508.0    | 23.59        | 7.40          |
| spirit-router            | 0.5.0   | ✓      | 39692.0    | 24.70        | 7.08          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38460.0    | 25.50        | 6.86          |
| total.js                 | 3.4.13  | ✓      | 38015.8    | 25.80        | 11.64         |
| restify                  | 8.6.1   | ✓      | 37792.6    | 25.96        | 6.81          |
| take-five                | 2.0.0   | ✓      | 37671.0    | 26.04        | 13.54         |
| koa-router               | 12.0.1  | ✓      | 36067.8    | 27.23        | 6.43          |
| hapi                     | 20.3.0  | ✓      | 32277.0    | 30.48        | 5.76          |
| microrouter              | 3.1.3   | ✓      | 30791.2    | 31.97        | 5.49          |
| trpc-router              | 9.27.3  | ✓      | 25675.6    | 38.44        | 5.68          |
| egg.js                   | 3.17.5  | ✓      | 17138.5    | 57.81        | 6.13          |
| express                  | 4.18.2  | ✓      | 12998.6    | 76.38        | 2.32          |
| fastify-big-json         | 4.24.3  | ✓      | 12587.0    | 78.91        | 144.81        |
| express-with-middlewares | 4.18.2  | ✓      | 12196.6    | 81.43        | 4.54          |
| express-route-prefix     | 4.18.2  | ✓      | 10914.0    | 91.03        | 4.04          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

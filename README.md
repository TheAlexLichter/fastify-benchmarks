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
* __Run:__ Mon May 13 2024 02:13:37 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68092.8    | 14.19        | 12.14         |
| polkadot                 | 1.0.0   | ✗      | 65903.2    | 14.68        | 11.75         |
| h3-router                | 0.8.6   | ✓      | 64025.6    | 15.13        | 10.50         |
| h3                       | 0.8.6   | ✗      | 63367.6    | 15.28        | 10.39         |
| bare                     | 10.13.0 | ✗      | 59693.6    | 16.25        | 10.65         |
| restana                  | 4.9.9   | ✓      | 58504.0    | 16.58        | 10.43         |
| foxify                   | 0.10.20 | ✓      | 58491.2    | 16.60        | 9.59          |
| polka                    | 0.5.2   | ✓      | 58228.0    | 16.67        | 10.38         |
| fastify                  | 4.27.0  | ✓      | 57208.8    | 16.99        | 10.26         |
| connect                  | 3.7.0   | ✗      | 56325.6    | 17.26        | 10.04         |
| micro                    | 9.4.1   | ✗      | 56007.2    | 17.36        | 9.99          |
| server-base-router       | 7.1.32  | ✓      | 54952.0    | 17.70        | 9.80          |
| server-base              | 7.1.32  | ✗      | 54272.8    | 17.93        | 9.68          |
| yeps                     | 1.1.1   | ✗      | 51970.4    | 18.74        | 9.27          |
| connect-router           | 1.3.8   | ✓      | 49593.6    | 19.67        | 8.84          |
| micro-route              | 2.5.0   | ✓      | 49260.8    | 19.79        | 8.78          |
| trek-engine              | 1.0.5   | ✗      | 48444.8    | 20.15        | 7.95          |
| trek-router              | 1.2.0   | ✓      | 46501.6    | 21.01        | 7.63          |
| vapr                     | 0.6.0   | ✓      | 45545.6    | 21.46        | 7.47          |
| yeps-router              | 1.2.0   | ✓      | 43535.2    | 22.47        | 7.76          |
| koa                      | 2.15.3  | ✗      | 42656.8    | 22.95        | 7.61          |
| spirit-router            | 0.5.0   | ✓      | 42034.4    | 23.29        | 7.50          |
| spirit                   | 0.6.1   | ✗      | 39968.0    | 24.52        | 7.13          |
| total.js                 | 3.4.13  | ✓      | 39804.8    | 24.62        | 12.19         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39319.0    | 24.93        | 7.01          |
| take-five                | 2.0.0   | ✓      | 38741.4    | 25.31        | 13.93         |
| restify                  | 8.6.1   | ✓      | 38086.2    | 25.76        | 6.86          |
| koa-router               | 12.0.1  | ✓      | 37405.0    | 26.23        | 6.67          |
| hapi                     | 20.3.0  | ✓      | 33778.0    | 29.09        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 31424.0    | 31.33        | 5.60          |
| trpc-router              | 9.27.4  | ✓      | 25824.4    | 38.21        | 5.71          |
| egg.js                   | 3.23.0  | ✓      | 17484.2    | 56.68        | 6.25          |
| express                  | 4.19.2  | ✓      | 13415.6    | 73.99        | 2.39          |
| fastify-big-json         | 4.27.0  | ✓      | 12849.8    | 77.29        | 147.84        |
| express-with-middlewares | 4.19.2  | ✓      | 12443.2    | 79.82        | 4.63          |
| express-route-prefix     | 4.19.2  | ✓      | 11144.2    | 89.17        | 4.12          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

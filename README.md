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
* __Run:__ Mon Jul 07 2025 03:11:47 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68966.8    | 14.00        | 12.30         |
| polkadot                 | 1.0.0   | ✗      | 68882.0    | 14.01        | 12.28         |
| h3                       | 0.8.6   | ✗      | 67309.6    | 14.37        | 11.04         |
| h3-router                | 0.8.6   | ✓      | 65594.0    | 14.75        | 10.76         |
| restana                  | 4.9.9   | ✓      | 61392.8    | 15.81        | 10.95         |
| bare                     | 10.13.0 | ✗      | 60693.6    | 15.98        | 10.82         |
| foxify                   | 0.10.20 | ✓      | 59407.2    | 16.33        | 9.74          |
| polka                    | 0.5.2   | ✓      | 58476.8    | 16.60        | 10.43         |
| connect                  | 3.7.0   | ✗      | 58424.0    | 16.62        | 10.42         |
| fastify                  | 4.29.1  | ✓      | 56477.6    | 17.21        | 10.13         |
| micro                    | 9.4.1   | ✗      | 56360.0    | 17.24        | 10.05         |
| server-base              | 7.1.32  | ✗      | 55049.6    | 17.67        | 9.82          |
| server-base-router       | 7.1.32  | ✓      | 54922.4    | 17.71        | 9.79          |
| yeps                     | 1.1.1   | ✗      | 51948.8    | 18.76        | 9.27          |
| connect-router           | 1.3.8   | ✓      | 50328.0    | 19.37        | 8.98          |
| micro-route              | 2.5.0   | ✓      | 50257.6    | 19.40        | 8.96          |
| trek-engine              | 1.0.5   | ✗      | 48316.8    | 20.20        | 7.93          |
| trek-router              | 1.2.0   | ✓      | 47525.6    | 20.54        | 7.80          |
| vapr                     | 0.6.0   | ✓      | 45753.6    | 21.35        | 7.51          |
| spirit                   | 0.6.1   | ✗      | 44854.4    | 21.83        | 8.00          |
| yeps-router              | 1.2.0   | ✓      | 43795.2    | 22.33        | 7.81          |
| spirit-router            | 0.5.0   | ✓      | 42601.6    | 22.97        | 7.60          |
| koa                      | 2.16.1  | ✗      | 42348.0    | 23.11        | 7.55          |
| total.js                 | 3.4.13  | ✓      | 39514.4    | 24.80        | 12.10         |
| take-five                | 2.0.0   | ✓      | 39311.4    | 24.94        | 14.13         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39093.0    | 25.08        | 6.97          |
| restify                  | 8.6.1   | ✓      | 38736.0    | 25.31        | 6.98          |
| koa-router               | 12.0.1  | ✓      | 36559.0    | 26.86        | 6.52          |
| hapi                     | 20.3.0  | ✓      | 33835.6    | 29.05        | 6.03          |
| microrouter              | 3.1.3   | ✓      | 32420.6    | 30.33        | 5.78          |
| trpc-router              | 9.27.4  | ✓      | 27513.6    | 35.84        | 6.09          |
| egg.js                   | 3.30.1  | ✓      | 17179.4    | 57.69        | 6.14          |
| express                  | 4.21.2  | ✓      | 13510.2    | 73.47        | 2.41          |
| fastify-big-json         | 4.29.1  | ✓      | 12919.8    | 76.87        | 148.64        |
| express-with-middlewares | 4.21.2  | ✓      | 12378.4    | 80.23        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 11100.2    | 89.53        | 4.11          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

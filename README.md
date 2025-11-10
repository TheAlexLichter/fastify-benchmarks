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
* __Run:__ Mon Nov 10 2025 02:58:53 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67235.2    | 14.38        | 11.99         |
| 0http                    | 3.5.3   | ✓      | 67170.0    | 14.39        | 11.98         |
| h3-router                | 0.8.6   | ✓      | 61570.4    | 15.74        | 10.10         |
| h3                       | 0.8.6   | ✗      | 60569.6    | 16.02        | 9.94          |
| restana                  | 4.9.9   | ✓      | 59776.0    | 16.21        | 10.66         |
| bare                     | 10.13.0 | ✗      | 59011.2    | 16.44        | 10.52         |
| foxify                   | 0.10.20 | ✓      | 56914.4    | 17.07        | 9.34          |
| polka                    | 0.5.2   | ✓      | 56444.8    | 17.22        | 10.07         |
| connect                  | 3.7.0   | ✗      | 55814.4    | 17.42        | 9.95          |
| fastify                  | 4.29.1  | ✓      | 55192.8    | 17.63        | 9.89          |
| micro                    | 9.4.1   | ✗      | 54596.0    | 17.82        | 9.74          |
| server-base              | 7.1.32  | ✗      | 54201.6    | 17.95        | 9.67          |
| yeps                     | 1.1.1   | ✗      | 52931.2    | 18.40        | 9.44          |
| server-base-router       | 7.1.32  | ✓      | 52892.0    | 18.41        | 9.43          |
| connect-router           | 1.3.8   | ✓      | 49914.4    | 19.54        | 8.90          |
| micro-route              | 2.5.0   | ✓      | 49766.4    | 19.60        | 8.87          |
| trek-engine              | 1.0.5   | ✗      | 48118.6    | 20.28        | 7.89          |
| trek-router              | 1.2.0   | ✓      | 47696.0    | 20.47        | 7.82          |
| vapr                     | 0.6.0   | ✓      | 45979.2    | 21.25        | 7.54          |
| yeps-router              | 1.2.0   | ✓      | 44111.2    | 22.18        | 7.87          |
| spirit                   | 0.6.1   | ✗      | 43408.0    | 22.55        | 7.74          |
| koa                      | 2.16.3  | ✗      | 41699.2    | 23.48        | 7.44          |
| spirit-router            | 0.5.0   | ✓      | 41381.6    | 23.67        | 7.38          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38656.6    | 25.37        | 6.89          |
| total.js                 | 3.4.13  | ✓      | 38255.2    | 25.64        | 11.71         |
| restify                  | 8.6.1   | ✓      | 38231.0    | 25.65        | 6.89          |
| take-five                | 2.0.0   | ✓      | 37848.2    | 25.93        | 13.61         |
| koa-router               | 12.0.1  | ✓      | 35804.6    | 27.43        | 6.39          |
| hapi                     | 20.3.0  | ✓      | 31222.0    | 31.52        | 5.57          |
| microrouter              | 3.1.3   | ✓      | 30527.6    | 32.25        | 5.44          |
| trpc-router              | 9.27.4  | ✓      | 26882.4    | 36.69        | 5.95          |
| egg.js                   | 3.31.0  | ✓      | 16913.3    | 58.59        | 6.05          |
| express                  | 4.21.2  | ✓      | 13101.0    | 75.79        | 2.34          |
| fastify-big-json         | 4.29.1  | ✓      | 12223.0    | 81.26        | 140.62        |
| express-with-middlewares | 4.21.2  | ✓      | 11849.6    | 83.83        | 4.41          |
| express-route-prefix     | 4.21.2  | ✓      | 10442.9    | 95.16        | 3.86          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

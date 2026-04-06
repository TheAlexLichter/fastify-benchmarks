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
* __Run:__ Mon Apr 06 2026 04:21:55 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 65403.6    | 14.79        | 11.66         |
| 0http                    | 3.5.3   | ✓      | 64812.4    | 14.93        | 11.56         |
| h3                       | 0.8.6   | ✗      | 61347.2    | 15.80        | 10.06         |
| restana                  | 4.9.9   | ✓      | 59226.4    | 16.38        | 10.56         |
| bare                     | 10.13.0 | ✗      | 58556.0    | 16.58        | 10.44         |
| h3-router                | 0.8.6   | ✓      | 57910.4    | 16.77        | 9.50          |
| foxify                   | 0.10.20 | ✓      | 57469.6    | 16.90        | 9.43          |
| polka                    | 0.5.2   | ✓      | 57172.8    | 16.99        | 10.20         |
| connect                  | 3.7.0   | ✗      | 55158.6    | 17.64        | 9.84          |
| micro                    | 9.4.1   | ✗      | 55021.6    | 17.68        | 9.81          |
| fastify                  | 4.29.1  | ✓      | 54663.2    | 17.79        | 9.80          |
| yeps                     | 1.1.1   | ✗      | 51973.6    | 18.75        | 9.27          |
| server-base              | 7.1.32  | ✗      | 51855.2    | 18.79        | 9.25          |
| server-base-router       | 7.1.32  | ✓      | 49880.8    | 19.55        | 8.89          |
| connect-router           | 1.3.8   | ✓      | 49807.2    | 19.58        | 8.88          |
| micro-route              | 2.5.0   | ✓      | 48788.0    | 20.01        | 8.70          |
| trek-engine              | 1.0.5   | ✗      | 47984.8    | 20.34        | 7.87          |
| trek-router              | 1.2.0   | ✓      | 46188.8    | 21.15        | 7.58          |
| vapr                     | 0.6.0   | ✓      | 46010.4    | 21.24        | 7.55          |
| yeps-router              | 1.2.0   | ✓      | 43684.0    | 22.39        | 7.79          |
| koa                      | 2.16.4  | ✗      | 41098.2    | 23.83        | 7.33          |
| total.js                 | 3.4.13  | ✓      | 39260.0    | 24.97        | 12.02         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38437.8    | 25.52        | 6.85          |
| restify                  | 8.6.1   | ✓      | 37583.0    | 26.11        | 6.77          |
| take-five                | 2.0.0   | ✓      | 37495.8    | 26.17        | 13.48         |
| koa-router               | 12.0.1  | ✓      | 35768.2    | 27.45        | 6.38          |
| spirit                   | 0.6.1   | ✗      | 34201.0    | 28.74        | 6.10          |
| spirit-router            | 0.5.0   | ✓      | 33052.8    | 29.75        | 5.89          |
| hapi                     | 20.3.0  | ✓      | 31992.2    | 30.76        | 5.71          |
| microrouter              | 3.1.3   | ✓      | 31672.2    | 31.07        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 26780.4    | 36.83        | 5.93          |
| egg.js                   | 3.34.0  | ✓      | 17252.2    | 57.45        | 6.17          |
| express                  | 4.22.1  | ✓      | 13041.6    | 76.11        | 2.33          |
| express-with-middlewares | 4.22.1  | ✓      | 12287.8    | 80.82        | 4.57          |
| fastify-big-json         | 4.29.1  | ✓      | 12185.2    | 81.52        | 140.20        |
| express-route-prefix     | 4.22.1  | ✓      | 10484.9    | 94.78        | 3.88          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

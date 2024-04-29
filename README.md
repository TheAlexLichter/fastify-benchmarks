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
* __Run:__ Mon Apr 29 2024 02:11:00 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 63962.8    | 15.14        | 11.41         |
| polkadot                 | 1.0.0   | ✗      | 60730.4    | 15.96        | 10.83         |
| bare                     | 10.13.0 | ✗      | 57619.2    | 16.86        | 10.28         |
| h3-router                | 0.8.6   | ✓      | 56447.2    | 17.21        | 9.26          |
| restana                  | 4.9.9   | ✓      | 55040.8    | 17.71        | 9.82          |
| h3                       | 0.8.6   | ✗      | 54936.8    | 17.69        | 9.01          |
| polka                    | 0.5.2   | ✓      | 54011.2    | 18.02        | 9.63          |
| foxify                   | 0.10.20 | ✓      | 53766.4    | 18.11        | 8.82          |
| fastify                  | 4.26.2  | ✓      | 52792.8    | 18.45        | 9.47          |
| connect                  | 3.7.0   | ✗      | 52710.4    | 18.48        | 9.40          |
| micro                    | 9.4.1   | ✗      | 51568.8    | 18.89        | 9.20          |
| server-base-router       | 7.1.32  | ✓      | 50262.4    | 19.40        | 8.96          |
| server-base              | 7.1.32  | ✗      | 50060.0    | 19.48        | 8.93          |
| yeps                     | 1.1.1   | ✗      | 49939.2    | 19.53        | 8.91          |
| connect-router           | 1.3.8   | ✓      | 47176.0    | 20.71        | 8.41          |
| micro-route              | 2.5.0   | ✓      | 46117.6    | 21.19        | 8.22          |
| trek-engine              | 1.0.5   | ✗      | 45173.8    | 21.64        | 7.41          |
| trek-router              | 1.2.0   | ✓      | 44316.8    | 22.06        | 7.27          |
| vapr                     | 0.6.0   | ✓      | 43455.2    | 22.52        | 7.13          |
| yeps-router              | 1.2.0   | ✓      | 42398.4    | 23.08        | 7.56          |
| koa                      | 2.15.3  | ✗      | 40475.8    | 24.21        | 7.22          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38293.8    | 25.62        | 6.83          |
| spirit                   | 0.6.1   | ✗      | 38122.4    | 25.74        | 6.80          |
| spirit-router            | 0.5.0   | ✓      | 37722.2    | 26.01        | 6.73          |
| total.js                 | 3.4.13  | ✓      | 37714.2    | 26.02        | 11.55         |
| take-five                | 2.0.0   | ✓      | 37259.0    | 26.34        | 13.40         |
| restify                  | 8.6.1   | ✓      | 37015.4    | 26.51        | 6.67          |
| koa-router               | 12.0.1  | ✓      | 35390.6    | 27.75        | 6.31          |
| hapi                     | 20.3.0  | ✓      | 32059.8    | 30.69        | 5.72          |
| microrouter              | 3.1.3   | ✓      | 30572.4    | 32.20        | 5.45          |
| trpc-router              | 9.27.4  | ✓      | 25835.2    | 38.20        | 5.72          |
| egg.js                   | 3.22.0  | ✓      | 16628.1    | 59.62        | 5.95          |
| express                  | 4.19.2  | ✓      | 13128.0    | 75.60        | 2.34          |
| fastify-big-json         | 4.26.2  | ✓      | 12408.8    | 80.01        | 142.76        |
| express-with-middlewares | 4.19.2  | ✓      | 12058.2    | 82.36        | 4.48          |
| express-route-prefix     | 4.19.2  | ✓      | 10737.0    | 92.56        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

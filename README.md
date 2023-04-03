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

* __Machine:__ linux x64 | 2 vCPUs | 6.8GB Mem
* __Node:__ `v14.21.3`
* __Run:__ Mon Apr 03 2023 02:16:56 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 33695.0    | 29.21        | 6.01          |
| bare                     | 10.13.0 | ✗      | 31795.8    | 31.02        | 5.67          |
| micro                    | 9.4.1   | ✗      | 30811.8    | 31.98        | 5.49          |
| polka                    | 0.5.2   | ✓      | 30681.6    | 32.11        | 5.47          |
| h3                       | 0.8.6   | ✗      | 29744.6    | 33.16        | 4.88          |
| h3-router                | 0.8.6   | ✓      | 29340.4    | 33.63        | 4.81          |
| foxify                   | 0.10.20 | ✓      | 28805.6    | 34.22        | 4.73          |
| server-base-router       | 7.1.32  | ✓      | 28409.2    | 34.70        | 5.07          |
| connect                  | 3.7.0   | ✗      | 28204.4    | 35.00        | 5.03          |
| 0http                    | 3.5.1   | ✓      | 27913.6    | 35.36        | 4.98          |
| server-base              | 7.1.32  | ✗      | 27362.4    | 36.06        | 4.88          |
| fastify                  | 4.15.0  | ✓      | 26947.2    | 36.65        | 4.83          |
| spirit-router            | 0.5.0   | ✓      | 26272.8    | 37.62        | 4.68          |
| restana                  | 4.9.7   | ✓      | 25899.6    | 38.11        | 4.62          |
| trek-router              | 1.2.0   | ✓      | 25513.2    | 38.69        | 4.19          |
| micro-route              | 2.5.0   | ✓      | 25179.6    | 39.21        | 4.49          |
| trek-engine              | 1.0.5   | ✗      | 25166.0    | 39.24        | 4.13          |
| connect-router           | 1.3.8   | ✓      | 24934.4    | 39.61        | 4.45          |
| spirit                   | 0.6.1   | ✗      | 24790.8    | 39.87        | 4.42          |
| koa                      | 2.14.1  | ✗      | 23441.6    | 42.14        | 4.18          |
| yeps                     | 1.1.1   | ✗      | 23409.6    | 42.21        | 4.17          |
| yeps-router              | 1.2.0   | ✓      | 23345.2    | 42.33        | 4.16          |
| vapr                     | 0.6.0   | ✓      | 22354.4    | 44.24        | 3.67          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 21668.7    | 45.64        | 3.86          |
| restify                  | 8.6.1   | ✓      | 21371.5    | 46.29        | 3.85          |
| take-five                | 2.0.0   | ✓      | 21094.0    | 46.91        | 7.58          |
| total.js                 | 3.4.13  | ✓      | 20576.0    | 48.11        | 6.30          |
| koa-router               | 12.0.0  | ✓      | 19091.5    | 51.87        | 3.40          |
| hapi                     | 20.3.0  | ✓      | 18577.5    | 53.31        | 3.31          |
| trpc-router              | 9.27.3  | ✓      | 18072.7    | 54.75        | 4.00          |
| microrouter              | 3.1.3   | ✓      | 17239.9    | 57.49        | 3.07          |
| egg.js                   | 3.15.0  | ✓      | 8565.8     | 116.26       | 3.06          |
| express                  | 4.18.2  | ✓      | 7375.3     | 134.92       | 1.32          |
| fastify-big-json         | 4.15.0  | ✓      | 6837.9     | 145.82       | 78.67         |
| express-route-prefix     | 4.18.2  | ✓      | 6622.7     | 150.37       | 2.45          |
| express-with-middlewares | 4.18.2  | ✓      | 6246.4     | 159.34       | 2.32          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

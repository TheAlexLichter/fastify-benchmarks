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
* __Run:__ Mon Jan 13 2025 02:43:47 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69538.0    | 13.88        | 12.40         |
| 0http                    | 3.5.3   | ✓      | 69390.8    | 13.92        | 12.37         |
| h3-router                | 0.8.6   | ✓      | 67013.6    | 14.41        | 10.99         |
| h3                       | 0.8.6   | ✗      | 66581.2    | 14.51        | 10.92         |
| restana                  | 4.9.9   | ✓      | 61388.8    | 15.78        | 10.95         |
| bare                     | 10.13.0 | ✗      | 59492.8    | 16.30        | 10.61         |
| polka                    | 0.5.2   | ✓      | 58312.0    | 16.65        | 10.40         |
| foxify                   | 0.10.20 | ✓      | 57868.8    | 16.78        | 9.49          |
| connect                  | 3.7.0   | ✗      | 56512.8    | 17.20        | 10.08         |
| micro                    | 9.4.1   | ✗      | 56216.8    | 17.29        | 10.03         |
| fastify                  | 4.29.0  | ✓      | 55145.6    | 17.64        | 9.89          |
| server-base              | 7.1.32  | ✗      | 53652.8    | 18.15        | 9.57          |
| server-base-router       | 7.1.32  | ✓      | 53157.6    | 18.32        | 9.48          |
| yeps                     | 1.1.1   | ✗      | 51729.6    | 18.84        | 9.22          |
| connect-router           | 1.3.8   | ✓      | 50619.2    | 19.26        | 9.03          |
| micro-route              | 2.5.0   | ✓      | 49563.2    | 19.67        | 8.84          |
| trek-engine              | 1.0.5   | ✗      | 47952.0    | 20.36        | 7.87          |
| trek-router              | 1.2.0   | ✓      | 47823.2    | 20.41        | 7.84          |
| vapr                     | 0.6.0   | ✓      | 45620.0    | 21.42        | 7.48          |
| spirit                   | 0.6.1   | ✗      | 44216.8    | 22.15        | 7.89          |
| spirit-router            | 0.5.0   | ✓      | 44013.6    | 22.19        | 7.85          |
| yeps-router              | 1.2.0   | ✓      | 43812.8    | 22.32        | 7.81          |
| koa                      | 2.15.3  | ✗      | 42521.6    | 23.03        | 7.58          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39775.4    | 24.64        | 7.09          |
| take-five                | 2.0.0   | ✓      | 39210.2    | 25.00        | 14.10         |
| total.js                 | 3.4.13  | ✓      | 39171.8    | 25.02        | 11.99         |
| restify                  | 8.6.1   | ✓      | 39141.8    | 25.05        | 7.06          |
| koa-router               | 12.0.1  | ✓      | 37842.2    | 25.93        | 6.75          |
| hapi                     | 20.3.0  | ✓      | 33088.0    | 29.72        | 5.90          |
| microrouter              | 3.1.3   | ✓      | 31886.8    | 30.87        | 5.69          |
| trpc-router              | 9.27.4  | ✓      | 27251.6    | 36.19        | 6.03          |
| egg.js                   | 3.30.0  | ✓      | 17472.6    | 56.71        | 6.25          |
| express                  | 4.21.2  | ✓      | 13566.2    | 73.18        | 2.42          |
| fastify-big-json         | 4.29.0  | ✓      | 12647.0    | 78.51        | 145.53        |
| express-with-middlewares | 4.21.2  | ✓      | 12349.2    | 80.42        | 4.59          |
| express-route-prefix     | 4.21.2  | ✓      | 10899.6    | 91.16        | 4.03          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

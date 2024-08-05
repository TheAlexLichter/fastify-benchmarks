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
* __Run:__ Mon Aug 05 2024 02:28:32 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66854.8    | 14.47        | 11.92         |
| h3                       | 0.8.6   | ✗      | 65038.8    | 14.87        | 10.67         |
| polkadot                 | 1.0.0   | ✗      | 64834.8    | 14.91        | 11.56         |
| h3-router                | 0.8.6   | ✓      | 62198.4    | 15.57        | 10.20         |
| bare                     | 10.13.0 | ✗      | 60440.0    | 16.06        | 10.78         |
| restana                  | 4.9.9   | ✓      | 59203.2    | 16.41        | 10.56         |
| foxify                   | 0.10.20 | ✓      | 59062.4    | 16.43        | 9.69          |
| polka                    | 0.5.2   | ✓      | 57312.0    | 16.95        | 10.22         |
| connect                  | 3.7.0   | ✗      | 56900.0    | 17.08        | 10.15         |
| micro                    | 9.4.1   | ✗      | 55702.4    | 17.46        | 9.93          |
| fastify                  | 4.28.1  | ✓      | 54268.8    | 17.93        | 9.73          |
| server-base-router       | 7.1.32  | ✓      | 53898.4    | 18.05        | 9.61          |
| server-base              | 7.1.32  | ✗      | 53207.2    | 18.30        | 9.49          |
| yeps                     | 1.1.1   | ✗      | 53030.4    | 18.36        | 9.46          |
| micro-route              | 2.5.0   | ✓      | 50409.6    | 19.33        | 8.99          |
| connect-router           | 1.3.8   | ✓      | 49896.8    | 19.55        | 8.90          |
| trek-engine              | 1.0.5   | ✗      | 48668.8    | 20.05        | 7.98          |
| vapr                     | 0.6.0   | ✓      | 46511.2    | 21.00        | 7.63          |
| trek-router              | 1.2.0   | ✓      | 46416.8    | 21.04        | 7.61          |
| yeps-router              | 1.2.0   | ✓      | 43815.2    | 22.32        | 7.81          |
| koa                      | 2.15.3  | ✗      | 42440.8    | 23.05        | 7.57          |
| spirit-router            | 0.5.0   | ✓      | 40720.8    | 24.07        | 7.26          |
| spirit                   | 0.6.1   | ✗      | 40171.2    | 24.37        | 7.16          |
| total.js                 | 3.4.13  | ✓      | 39155.0    | 25.04        | 11.99         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38776.6    | 25.29        | 6.92          |
| take-five                | 2.0.0   | ✓      | 38494.6    | 25.48        | 13.84         |
| restify                  | 8.6.1   | ✓      | 38265.4    | 25.63        | 6.90          |
| koa-router               | 12.0.1  | ✓      | 37933.0    | 25.86        | 6.76          |
| hapi                     | 20.3.0  | ✓      | 33277.0    | 29.55        | 5.93          |
| microrouter              | 3.1.3   | ✓      | 32413.8    | 30.33        | 5.78          |
| trpc-router              | 9.27.4  | ✓      | 26529.2    | 37.19        | 5.87          |
| egg.js                   | 3.27.1  | ✓      | 16750.4    | 59.17        | 5.99          |
| express                  | 4.19.2  | ✓      | 13359.0    | 74.31        | 2.38          |
| fastify-big-json         | 4.28.1  | ✓      | 13025.8    | 76.21        | 149.86        |
| express-with-middlewares | 4.19.2  | ✓      | 12281.2    | 80.86        | 4.57          |
| express-route-prefix     | 4.19.2  | ✓      | 10724.4    | 92.65        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

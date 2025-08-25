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
* __Run:__ Mon Aug 25 2025 02:57:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 62920.0    | 15.40        | 11.22         |
| polkadot                 | 1.0.0   | ✗      | 61533.6    | 15.76        | 10.97         |
| h3                       | 0.8.6   | ✗      | 59350.4    | 16.35        | 9.73          |
| h3-router                | 0.8.6   | ✓      | 59206.4    | 16.40        | 9.71          |
| bare                     | 10.13.0 | ✗      | 57337.6    | 16.94        | 10.23         |
| restana                  | 4.9.9   | ✓      | 56352.8    | 17.26        | 10.05         |
| polka                    | 0.5.2   | ✓      | 56284.8    | 17.27        | 10.04         |
| connect                  | 3.7.0   | ✗      | 55488.0    | 17.53        | 9.90          |
| foxify                   | 0.10.20 | ✓      | 55058.4    | 17.66        | 9.03          |
| micro                    | 9.4.1   | ✗      | 53721.6    | 18.12        | 9.58          |
| fastify                  | 4.29.1  | ✓      | 53450.4    | 18.21        | 9.58          |
| server-base-router       | 7.1.32  | ✓      | 52858.4    | 18.43        | 9.43          |
| server-base              | 7.1.32  | ✗      | 51465.6    | 18.94        | 9.18          |
| yeps                     | 1.1.1   | ✗      | 50368.8    | 19.35        | 8.98          |
| micro-route              | 2.5.0   | ✓      | 48512.8    | 20.12        | 8.65          |
| connect-router           | 1.3.8   | ✓      | 48192.0    | 20.26        | 8.59          |
| trek-router              | 1.2.0   | ✓      | 45498.4    | 21.48        | 7.46          |
| vapr                     | 0.6.0   | ✓      | 45207.2    | 21.62        | 7.42          |
| trek-engine              | 1.0.5   | ✗      | 45195.0    | 21.63        | 7.41          |
| yeps-router              | 1.2.0   | ✓      | 42276.0    | 23.16        | 7.54          |
| koa                      | 2.16.2  | ✗      | 40698.2    | 24.07        | 7.26          |
| spirit                   | 0.6.1   | ✗      | 40333.6    | 24.30        | 7.19          |
| spirit-router            | 0.5.0   | ✓      | 38617.0    | 25.40        | 6.89          |
| total.js                 | 3.4.13  | ✓      | 38613.4    | 25.40        | 11.82         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37793.8    | 25.96        | 6.74          |
| take-five                | 2.0.0   | ✓      | 37557.4    | 26.13        | 13.50         |
| restify                  | 8.6.1   | ✓      | 36995.8    | 26.53        | 6.67          |
| koa-router               | 12.0.1  | ✓      | 35475.8    | 27.68        | 6.33          |
| hapi                     | 20.3.0  | ✓      | 31703.6    | 31.03        | 5.65          |
| microrouter              | 3.1.3   | ✓      | 31069.2    | 31.68        | 5.54          |
| trpc-router              | 9.27.4  | ✓      | 26460.8    | 37.28        | 5.85          |
| egg.js                   | 3.31.0  | ✓      | 16551.2    | 59.88        | 5.92          |
| express                  | 4.21.2  | ✓      | 13414.6    | 74.00        | 2.39          |
| fastify-big-json         | 4.29.1  | ✓      | 12459.6    | 79.74        | 143.36        |
| express-with-middlewares | 4.21.2  | ✓      | 11997.4    | 82.79        | 4.46          |
| express-route-prefix     | 4.21.2  | ✓      | 10557.0    | 94.13        | 3.91          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

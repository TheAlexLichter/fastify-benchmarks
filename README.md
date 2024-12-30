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
* __Run:__ Mon Dec 30 2024 02:41:15 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69682.8    | 13.85        | 12.43         |
| polkadot                 | 1.0.0   | ✗      | 68821.6    | 14.03        | 12.27         |
| h3                       | 0.8.6   | ✗      | 66696.4    | 14.49        | 10.94         |
| restana                  | 4.9.9   | ✓      | 62712.0    | 15.46        | 11.18         |
| h3-router                | 0.8.6   | ✓      | 62376.8    | 15.54        | 10.23         |
| bare                     | 10.13.0 | ✗      | 60574.4    | 16.00        | 10.80         |
| connect                  | 3.7.0   | ✗      | 57704.8    | 16.84        | 10.29         |
| foxify                   | 0.10.20 | ✓      | 57628.8    | 16.86        | 9.45          |
| polka                    | 0.5.2   | ✓      | 56637.6    | 17.15        | 10.10         |
| micro                    | 9.4.1   | ✗      | 55605.6    | 17.48        | 9.92          |
| fastify                  | 4.29.0  | ✓      | 55602.4    | 17.48        | 9.97          |
| server-base              | 7.1.32  | ✗      | 54185.6    | 17.96        | 9.66          |
| server-base-router       | 7.1.32  | ✓      | 53990.4    | 18.02        | 9.63          |
| yeps                     | 1.1.1   | ✗      | 52220.8    | 18.66        | 9.31          |
| connect-router           | 1.3.8   | ✓      | 50890.4    | 19.15        | 9.08          |
| micro-route              | 2.5.0   | ✓      | 49288.8    | 19.78        | 8.79          |
| trek-engine              | 1.0.5   | ✗      | 49248.8    | 19.81        | 8.08          |
| trek-router              | 1.2.0   | ✓      | 48432.8    | 20.15        | 7.94          |
| vapr                     | 0.6.0   | ✓      | 46592.8    | 20.97        | 7.64          |
| spirit                   | 0.6.1   | ✗      | 44656.0    | 21.90        | 7.96          |
| yeps-router              | 1.2.0   | ✓      | 44180.8    | 22.13        | 7.88          |
| koa                      | 2.15.3  | ✗      | 42616.0    | 22.96        | 7.60          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40729.6    | 24.06        | 7.26          |
| total.js                 | 3.4.13  | ✓      | 40533.6    | 24.17        | 12.41         |
| restify                  | 8.6.1   | ✓      | 39539.0    | 24.80        | 7.13          |
| take-five                | 2.0.0   | ✓      | 38097.8    | 25.75        | 13.70         |
| koa-router               | 12.0.1  | ✓      | 37800.6    | 25.95        | 6.74          |
| spirit-router            | 0.5.0   | ✓      | 35790.6    | 27.46        | 6.38          |
| hapi                     | 20.3.0  | ✓      | 34198.6    | 28.74        | 6.10          |
| microrouter              | 3.1.3   | ✓      | 32262.0    | 30.49        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 27417.2    | 35.97        | 6.07          |
| egg.js                   | 3.29.0  | ✓      | 17473.9    | 56.71        | 6.25          |
| express                  | 4.21.2  | ✓      | 13614.2    | 72.89        | 2.43          |
| fastify-big-json         | 4.29.0  | ✓      | 12870.8    | 77.15        | 148.08        |
| express-with-middlewares | 4.21.2  | ✓      | 12731.2    | 77.99        | 4.74          |
| express-route-prefix     | 4.21.2  | ✓      | 10997.4    | 90.34        | 4.07          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jan 06 2025 02:43:04 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68228.0    | 14.16        | 12.17         |
| polkadot                 | 1.0.0   | ✗      | 64458.0    | 15.02        | 11.50         |
| h3                       | 0.8.6   | ✗      | 60741.6    | 15.96        | 9.96          |
| bare                     | 10.13.0 | ✗      | 60037.6    | 16.15        | 10.71         |
| restana                  | 4.9.9   | ✓      | 58346.4    | 16.64        | 10.41         |
| h3-router                | 0.8.6   | ✓      | 57842.4    | 16.79        | 9.49          |
| foxify                   | 0.10.20 | ✓      | 57172.8    | 16.99        | 9.38          |
| connect                  | 3.7.0   | ✗      | 56844.0    | 17.09        | 10.14         |
| fastify                  | 4.29.0  | ✓      | 55433.6    | 17.54        | 9.94          |
| polka                    | 0.5.2   | ✓      | 54398.4    | 17.89        | 9.70          |
| micro                    | 9.4.1   | ✗      | 53449.6    | 18.21        | 9.53          |
| server-base-router       | 7.1.32  | ✓      | 51752.0    | 18.83        | 9.23          |
| yeps                     | 1.1.1   | ✗      | 51372.0    | 18.97        | 9.16          |
| server-base              | 7.1.32  | ✗      | 50866.4    | 19.16        | 9.07          |
| micro-route              | 2.5.0   | ✓      | 48557.6    | 20.09        | 8.66          |
| connect-router           | 1.3.8   | ✓      | 48057.6    | 20.31        | 8.57          |
| trek-engine              | 1.0.5   | ✗      | 48024.8    | 20.33        | 7.88          |
| trek-router              | 1.2.0   | ✓      | 47329.6    | 20.63        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 44943.2    | 21.75        | 7.37          |
| yeps-router              | 1.2.0   | ✓      | 43536.8    | 22.47        | 7.76          |
| spirit-router            | 0.5.0   | ✓      | 42934.4    | 22.79        | 7.66          |
| koa                      | 2.15.3  | ✗      | 40747.2    | 24.05        | 7.27          |
| total.js                 | 3.4.13  | ✓      | 38994.4    | 25.14        | 11.94         |
| take-five                | 2.0.0   | ✓      | 38638.2    | 25.39        | 13.89         |
| spirit                   | 0.6.1   | ✗      | 38508.0    | 25.47        | 6.87          |
| restify                  | 8.6.1   | ✓      | 38297.4    | 25.61        | 6.90          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38199.4    | 25.68        | 6.81          |
| koa-router               | 12.0.1  | ✓      | 35769.8    | 27.45        | 6.38          |
| hapi                     | 20.3.0  | ✓      | 31293.0    | 31.45        | 5.58          |
| microrouter              | 3.1.3   | ✓      | 30298.4    | 32.50        | 5.40          |
| trpc-router              | 9.27.4  | ✓      | 26908.8    | 36.65        | 5.95          |
| egg.js                   | 3.29.0  | ✓      | 16799.9    | 59.00        | 6.01          |
| express                  | 4.21.2  | ✓      | 13313.8    | 74.57        | 2.37          |
| fastify-big-json         | 4.29.0  | ✓      | 12586.8    | 78.91        | 144.81        |
| express-with-middlewares | 4.21.2  | ✓      | 12494.8    | 79.48        | 4.65          |
| express-route-prefix     | 4.21.2  | ✓      | 10583.8    | 93.90        | 3.92          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jul 29 2024 02:28:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67902.8    | 14.22        | 12.11         |
| 0http                    | 3.5.3   | ✓      | 63690.8    | 15.20        | 11.36         |
| h3-router                | 0.8.6   | ✓      | 60372.8    | 16.07        | 9.90          |
| restana                  | 4.9.9   | ✓      | 60333.6    | 16.10        | 10.76         |
| h3                       | 0.8.6   | ✗      | 59824.0    | 16.23        | 9.81          |
| bare                     | 10.13.0 | ✗      | 58581.6    | 16.57        | 10.45         |
| foxify                   | 0.10.20 | ✓      | 57775.2    | 16.80        | 9.48          |
| polka                    | 0.5.2   | ✓      | 57483.2    | 16.90        | 10.25         |
| connect                  | 3.7.0   | ✗      | 55825.6    | 17.42        | 9.96          |
| micro                    | 9.4.1   | ✗      | 54236.8    | 17.94        | 9.67          |
| server-base              | 7.1.32  | ✗      | 54222.4    | 17.95        | 9.67          |
| fastify                  | 4.28.1  | ✓      | 54095.2    | 17.99        | 9.70          |
| server-base-router       | 7.1.32  | ✓      | 53700.8    | 18.12        | 9.58          |
| yeps                     | 1.1.1   | ✗      | 50960.0    | 19.12        | 9.09          |
| micro-route              | 2.5.0   | ✓      | 50472.8    | 19.31        | 9.00          |
| trek-engine              | 1.0.5   | ✗      | 47536.8    | 20.54        | 7.80          |
| connect-router           | 1.3.8   | ✓      | 47273.6    | 20.66        | 8.43          |
| trek-router              | 1.2.0   | ✓      | 46644.0    | 20.94        | 7.65          |
| vapr                     | 0.6.0   | ✓      | 45192.0    | 21.63        | 7.41          |
| spirit                   | 0.6.1   | ✗      | 43183.2    | 22.64        | 7.70          |
| yeps-router              | 1.2.0   | ✓      | 43095.2    | 22.71        | 7.69          |
| koa                      | 2.15.3  | ✗      | 41603.2    | 23.53        | 7.42          |
| spirit-router            | 0.5.0   | ✓      | 41308.8    | 23.70        | 7.37          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38856.6    | 25.23        | 6.93          |
| restify                  | 8.6.1   | ✓      | 38609.0    | 25.40        | 6.96          |
| take-five                | 2.0.0   | ✓      | 38108.2    | 25.74        | 13.70         |
| total.js                 | 3.4.13  | ✓      | 38056.6    | 25.77        | 11.65         |
| koa-router               | 12.0.1  | ✓      | 35381.6    | 27.76        | 6.31          |
| hapi                     | 20.3.0  | ✓      | 31934.0    | 30.81        | 5.70          |
| microrouter              | 3.1.3   | ✓      | 31340.0    | 31.41        | 5.59          |
| trpc-router              | 9.27.4  | ✓      | 25765.2    | 38.30        | 5.70          |
| egg.js                   | 3.27.1  | ✓      | 17020.5    | 58.23        | 6.09          |
| express                  | 4.19.2  | ✓      | 13286.8    | 74.71        | 2.37          |
| fastify-big-json         | 4.28.1  | ✓      | 12721.6    | 78.06        | 146.37        |
| express-with-middlewares | 4.19.2  | ✓      | 12151.4    | 81.75        | 4.52          |
| express-route-prefix     | 4.19.2  | ✓      | 10836.2    | 91.69        | 4.01          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jan 27 2025 02:37:46 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69733.2    | 13.84        | 12.44         |
| 0http                    | 3.5.3   | ✓      | 68675.6    | 14.06        | 12.25         |
| h3                       | 0.8.6   | ✗      | 68235.2    | 14.18        | 11.19         |
| h3-router                | 0.8.6   | ✓      | 65345.6    | 14.81        | 10.72         |
| bare                     | 10.13.0 | ✗      | 62098.4    | 15.62        | 11.07         |
| restana                  | 4.9.9   | ✓      | 60388.8    | 16.07        | 10.77         |
| foxify                   | 0.10.20 | ✓      | 60369.6    | 16.07        | 9.90          |
| polka                    | 0.5.2   | ✓      | 58663.2    | 16.55        | 10.46         |
| fastify                  | 4.29.0  | ✓      | 56872.0    | 17.09        | 10.20         |
| micro                    | 9.4.1   | ✗      | 56491.2    | 17.20        | 10.07         |
| connect                  | 3.7.0   | ✗      | 56204.8    | 17.29        | 10.02         |
| server-base-router       | 7.1.32  | ✓      | 55267.2    | 17.60        | 9.86          |
| server-base              | 7.1.32  | ✗      | 54722.4    | 17.77        | 9.76          |
| yeps                     | 1.1.1   | ✗      | 54134.4    | 17.98        | 9.65          |
| connect-router           | 1.3.8   | ✓      | 50411.2    | 19.34        | 8.99          |
| micro-route              | 2.5.0   | ✓      | 49909.6    | 19.53        | 8.90          |
| trek-engine              | 1.0.5   | ✗      | 48864.0    | 19.97        | 8.01          |
| trek-router              | 1.2.0   | ✓      | 47570.4    | 20.53        | 7.80          |
| vapr                     | 0.6.0   | ✓      | 45440.0    | 21.50        | 7.45          |
| spirit                   | 0.6.1   | ✗      | 44744.8    | 21.92        | 7.98          |
| yeps-router              | 1.2.0   | ✓      | 44134.4    | 22.16        | 7.87          |
| spirit-router            | 0.5.0   | ✓      | 44071.2    | 22.19        | 7.86          |
| koa                      | 2.15.3  | ✗      | 42386.4    | 23.09        | 7.56          |
| total.js                 | 3.4.13  | ✓      | 39906.4    | 24.57        | 12.22         |
| restify                  | 8.6.1   | ✓      | 39656.0    | 24.71        | 7.15          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39387.4    | 24.89        | 7.02          |
| take-five                | 2.0.0   | ✓      | 38314.2    | 25.60        | 13.78         |
| koa-router               | 12.0.1  | ✓      | 38031.8    | 25.79        | 6.78          |
| hapi                     | 20.3.0  | ✓      | 34748.6    | 28.28        | 6.20          |
| microrouter              | 3.1.3   | ✓      | 32230.0    | 30.53        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 27455.2    | 35.92        | 6.07          |
| egg.js                   | 3.30.1  | ✓      | 17374.8    | 57.04        | 6.21          |
| express                  | 4.21.2  | ✓      | 13411.0    | 73.99        | 2.39          |
| fastify-big-json         | 4.29.0  | ✓      | 12676.8    | 78.34        | 145.85        |
| express-with-middlewares | 4.21.2  | ✓      | 12396.2    | 80.12        | 4.61          |
| express-route-prefix     | 4.21.2  | ✓      | 10911.4    | 91.05        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

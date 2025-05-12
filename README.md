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
* __Run:__ Mon May 12 2025 02:57:58 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69288.0    | 13.93        | 12.36         |
| 0http                    | 3.5.3   | ✓      | 68641.2    | 14.07        | 12.24         |
| h3-router                | 0.8.6   | ✓      | 66764.4    | 14.48        | 10.95         |
| h3                       | 0.8.6   | ✗      | 66128.4    | 14.62        | 10.85         |
| restana                  | 4.9.9   | ✓      | 60668.0    | 15.99        | 10.82         |
| bare                     | 10.13.0 | ✗      | 59794.4    | 16.23        | 10.66         |
| foxify                   | 0.10.20 | ✓      | 59311.2    | 16.37        | 9.73          |
| connect                  | 3.7.0   | ✗      | 57859.2    | 16.78        | 10.32         |
| polka                    | 0.5.2   | ✓      | 57100.8    | 17.01        | 10.18         |
| micro                    | 9.4.1   | ✗      | 55023.2    | 17.68        | 9.81          |
| fastify                  | 4.29.1  | ✓      | 54639.2    | 17.81        | 9.80          |
| server-base-router       | 7.1.32  | ✓      | 54544.0    | 17.84        | 9.73          |
| server-base              | 7.1.32  | ✗      | 53784.8    | 18.09        | 9.59          |
| yeps                     | 1.1.1   | ✗      | 52633.6    | 18.51        | 9.39          |
| micro-route              | 2.5.0   | ✓      | 49976.8    | 19.50        | 8.91          |
| connect-router           | 1.3.8   | ✓      | 49364.0    | 19.76        | 8.80          |
| trek-router              | 1.2.0   | ✓      | 48121.6    | 20.28        | 7.89          |
| trek-engine              | 1.0.5   | ✗      | 48042.4    | 20.32        | 7.88          |
| vapr                     | 0.6.0   | ✓      | 46509.6    | 21.01        | 7.63          |
| yeps-router              | 1.2.0   | ✓      | 43440.0    | 22.52        | 7.75          |
| spirit                   | 0.6.1   | ✗      | 43428.8    | 22.52        | 7.75          |
| spirit-router            | 0.5.0   | ✓      | 42511.2    | 23.02        | 7.58          |
| koa                      | 2.16.1  | ✗      | 41504.2    | 23.58        | 7.40          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39398.2    | 24.88        | 7.03          |
| total.js                 | 3.4.13  | ✓      | 39376.8    | 24.90        | 12.05         |
| restify                  | 8.6.1   | ✓      | 38478.2    | 25.50        | 6.94          |
| take-five                | 2.0.0   | ✓      | 37824.6    | 25.94        | 13.60         |
| koa-router               | 12.0.1  | ✓      | 36859.8    | 26.62        | 6.57          |
| hapi                     | 20.3.0  | ✓      | 33773.8    | 29.11        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 31011.2    | 31.75        | 5.53          |
| trpc-router              | 9.27.4  | ✓      | 27351.6    | 36.06        | 6.05          |
| egg.js                   | 3.30.1  | ✓      | 17220.7    | 57.55        | 6.16          |
| express                  | 4.21.2  | ✓      | 13651.4    | 72.71        | 2.43          |
| fastify-big-json         | 4.29.1  | ✓      | 12754.4    | 77.86        | 146.75        |
| express-with-middlewares | 4.21.2  | ✓      | 12461.0    | 79.70        | 4.63          |
| express-route-prefix     | 4.21.2  | ✓      | 10984.0    | 90.45        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

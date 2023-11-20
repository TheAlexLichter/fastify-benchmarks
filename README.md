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
* __Run:__ Mon Nov 20 2023 02:12:14 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 65349.6    | 14.79        | 11.65         |
| 0http                    | 3.5.2   | ✓      | 61134.4    | 15.88        | 10.90         |
| h3-router                | 0.8.6   | ✓      | 60979.2    | 15.92        | 10.00         |
| h3                       | 0.8.6   | ✗      | 60396.8    | 16.07        | 9.91          |
| bare                     | 10.13.0 | ✗      | 57709.6    | 16.83        | 10.29         |
| foxify                   | 0.10.20 | ✓      | 56439.2    | 17.22        | 9.26          |
| polka                    | 0.5.2   | ✓      | 55167.2    | 17.63        | 9.84          |
| fastify                  | 4.24.3  | ✓      | 54221.6    | 17.95        | 9.72          |
| micro                    | 9.4.1   | ✗      | 53348.8    | 18.25        | 9.51          |
| connect                  | 3.7.0   | ✗      | 53164.0    | 18.31        | 9.48          |
| server-base-router       | 7.1.32  | ✓      | 51604.0    | 18.88        | 9.20          |
| restana                  | 4.9.7   | ✓      | 50425.6    | 19.34        | 8.99          |
| server-base              | 7.1.32  | ✗      | 50171.2    | 19.44        | 8.95          |
| yeps                     | 1.1.1   | ✗      | 49836.8    | 19.57        | 8.89          |
| connect-router           | 1.3.8   | ✓      | 48331.2    | 20.19        | 8.62          |
| micro-route              | 2.5.0   | ✓      | 47656.0    | 20.50        | 8.50          |
| trek-engine              | 1.0.5   | ✗      | 46371.2    | 21.07        | 7.61          |
| trek-router              | 1.2.0   | ✓      | 45140.0    | 21.65        | 7.40          |
| vapr                     | 0.6.0   | ✓      | 44392.0    | 22.03        | 7.28          |
| yeps-router              | 1.2.0   | ✓      | 42961.6    | 22.78        | 7.66          |
| koa                      | 2.14.2  | ✗      | 41184.0    | 23.78        | 7.34          |
| spirit                   | 0.6.1   | ✗      | 40189.6    | 24.35        | 7.17          |
| spirit-router            | 0.5.0   | ✓      | 38700.0    | 25.38        | 6.90          |
| restify                  | 8.6.1   | ✓      | 38186.6    | 25.69        | 6.88          |
| total.js                 | 3.4.13  | ✓      | 38177.6    | 25.70        | 11.69         |
| take-five                | 2.0.0   | ✓      | 37751.8    | 25.98        | 13.57         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37643.0    | 26.06        | 6.71          |
| koa-router               | 12.0.1  | ✓      | 35204.2    | 27.90        | 6.28          |
| hapi                     | 20.3.0  | ✓      | 31888.0    | 30.85        | 5.69          |
| microrouter              | 3.1.3   | ✓      | 31338.8    | 31.41        | 5.59          |
| trpc-router              | 9.27.3  | ✓      | 25642.0    | 38.49        | 5.67          |
| egg.js                   | 3.17.5  | ✓      | 17133.8    | 57.86        | 6.13          |
| express                  | 4.18.2  | ✓      | 13224.8    | 75.08        | 2.36          |
| fastify-big-json         | 4.24.3  | ✓      | 12810.8    | 77.49        | 147.40        |
| express-with-middlewares | 4.18.2  | ✓      | 12397.2    | 80.08        | 4.61          |
| express-route-prefix     | 4.18.2  | ✓      | 10947.8    | 90.76        | 4.05          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

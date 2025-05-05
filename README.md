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
* __Run:__ Mon May 05 2025 02:56:55 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 65534.0    | 14.77        | 11.69         |
| h3                       | 0.8.6   | ✗      | 64021.2    | 15.13        | 10.50         |
| polkadot                 | 1.0.0   | ✗      | 63946.0    | 15.14        | 11.40         |
| h3-router                | 0.8.6   | ✓      | 62142.8    | 15.60        | 10.19         |
| bare                     | 10.13.0 | ✗      | 58032.0    | 16.74        | 10.35         |
| foxify                   | 0.10.20 | ✓      | 57676.8    | 16.84        | 9.46          |
| polka                    | 0.5.2   | ✓      | 56283.2    | 17.27        | 10.04         |
| restana                  | 4.9.9   | ✓      | 56263.2    | 17.29        | 10.03         |
| connect                  | 3.7.0   | ✗      | 55964.0    | 17.38        | 9.98          |
| fastify                  | 4.29.1  | ✓      | 55749.6    | 17.44        | 10.00         |
| server-base              | 7.1.32  | ✗      | 55378.4    | 17.56        | 9.88          |
| micro                    | 9.4.1   | ✗      | 54057.6    | 18.00        | 9.64          |
| server-base-router       | 7.1.32  | ✓      | 52221.6    | 18.65        | 9.31          |
| yeps                     | 1.1.1   | ✗      | 51132.8    | 19.06        | 9.12          |
| connect-router           | 1.3.8   | ✓      | 48380.0    | 20.17        | 8.63          |
| micro-route              | 2.5.0   | ✓      | 48345.6    | 20.18        | 8.62          |
| trek-engine              | 1.0.5   | ✗      | 47744.0    | 20.45        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 46009.6    | 21.23        | 7.55          |
| vapr                     | 0.6.0   | ✓      | 44366.4    | 22.04        | 7.28          |
| spirit                   | 0.6.1   | ✗      | 43733.6    | 22.35        | 7.80          |
| yeps-router              | 1.2.0   | ✓      | 42538.4    | 23.00        | 7.59          |
| koa                      | 2.16.1  | ✗      | 41102.6    | 23.83        | 7.33          |
| total.js                 | 3.4.13  | ✓      | 38388.8    | 25.54        | 11.75         |
| take-five                | 2.0.0   | ✓      | 37871.8    | 25.91        | 13.62         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37415.8    | 26.23        | 6.67          |
| restify                  | 8.6.1   | ✓      | 36913.4    | 26.59        | 6.65          |
| koa-router               | 12.0.1  | ✓      | 35088.2    | 28.00        | 6.26          |
| spirit-router            | 0.5.0   | ✓      | 34921.2    | 28.13        | 6.23          |
| hapi                     | 20.3.0  | ✓      | 32349.0    | 30.41        | 5.77          |
| microrouter              | 3.1.3   | ✓      | 30284.8    | 32.52        | 5.40          |
| trpc-router              | 9.27.4  | ✓      | 26554.4    | 37.15        | 5.88          |
| egg.js                   | 3.30.1  | ✓      | 16762.4    | 59.14        | 5.99          |
| express                  | 4.21.2  | ✓      | 13451.6    | 73.80        | 2.40          |
| fastify-big-json         | 4.29.1  | ✓      | 12610.8    | 78.75        | 145.09        |
| express-with-middlewares | 4.21.2  | ✓      | 12484.2    | 79.54        | 4.64          |
| express-route-prefix     | 4.21.2  | ✓      | 10790.0    | 92.10        | 3.99          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

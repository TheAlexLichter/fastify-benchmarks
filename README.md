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
* __Run:__ Mon Aug 11 2025 03:16:59 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66426.0    | 14.56        | 11.85         |
| polkadot                 | 1.0.0   | ✗      | 65808.4    | 14.70        | 11.74         |
| h3                       | 0.8.6   | ✗      | 61543.2    | 15.75        | 10.10         |
| bare                     | 10.13.0 | ✗      | 60728.0    | 15.97        | 10.83         |
| h3-router                | 0.8.6   | ✓      | 60704.8    | 15.98        | 9.96          |
| foxify                   | 0.10.20 | ✓      | 58094.4    | 16.72        | 9.53          |
| restana                  | 4.9.9   | ✓      | 57898.4    | 16.78        | 10.33         |
| connect                  | 3.7.0   | ✗      | 57113.6    | 17.01        | 10.19         |
| polka                    | 0.5.2   | ✓      | 56946.4    | 17.06        | 10.16         |
| fastify                  | 4.29.1  | ✓      | 55432.8    | 17.55        | 9.94          |
| server-base              | 7.1.32  | ✗      | 55176.8    | 17.63        | 9.84          |
| server-base-router       | 7.1.32  | ✓      | 54490.4    | 17.85        | 9.72          |
| micro                    | 9.4.1   | ✗      | 54008.0    | 18.02        | 9.63          |
| yeps                     | 1.1.1   | ✗      | 51246.4    | 19.02        | 9.14          |
| connect-router           | 1.3.8   | ✓      | 49504.8    | 19.70        | 8.83          |
| micro-route              | 2.5.0   | ✓      | 49337.6    | 19.77        | 8.80          |
| trek-engine              | 1.0.5   | ✗      | 47244.0    | 20.66        | 7.75          |
| trek-router              | 1.2.0   | ✓      | 46856.0    | 20.85        | 7.69          |
| vapr                     | 0.6.0   | ✓      | 45892.0    | 21.29        | 7.53          |
| yeps-router              | 1.2.0   | ✓      | 42184.8    | 23.20        | 7.52          |
| spirit                   | 0.6.1   | ✗      | 41156.0    | 23.79        | 7.34          |
| koa                      | 2.16.2  | ✗      | 40511.2    | 24.19        | 7.22          |
| spirit-router            | 0.5.0   | ✓      | 39879.2    | 24.58        | 7.11          |
| total.js                 | 3.4.13  | ✓      | 38570.4    | 25.43        | 11.81         |
| take-five                | 2.0.0   | ✓      | 38502.6    | 25.47        | 13.84         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38469.8    | 25.50        | 6.86          |
| restify                  | 8.6.1   | ✓      | 38273.8    | 25.63        | 6.90          |
| koa-router               | 12.0.1  | ✓      | 35870.6    | 27.37        | 6.40          |
| hapi                     | 20.3.0  | ✓      | 32575.0    | 30.19        | 5.81          |
| microrouter              | 3.1.3   | ✓      | 31300.4    | 31.44        | 5.58          |
| trpc-router              | 9.27.4  | ✓      | 26296.4    | 37.52        | 5.82          |
| egg.js                   | 3.31.0  | ✓      | 16534.8    | 59.96        | 5.91          |
| express                  | 4.21.2  | ✓      | 13467.4    | 73.71        | 2.40          |
| express-with-middlewares | 4.21.2  | ✓      | 12650.4    | 78.49        | 4.70          |
| fastify-big-json         | 4.29.1  | ✓      | 12610.6    | 78.76        | 145.10        |
| express-route-prefix     | 4.21.2  | ✓      | 10739.0    | 92.55        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

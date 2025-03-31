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
* __Run:__ Mon Mar 31 2025 02:52:18 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68628.8    | 14.08        | 12.24         |
| polkadot                 | 1.0.0   | ✗      | 68331.6    | 14.15        | 12.19         |
| h3-router                | 0.8.6   | ✓      | 63774.8    | 15.18        | 10.46         |
| h3                       | 0.8.6   | ✗      | 61910.0    | 15.66        | 10.16         |
| restana                  | 4.9.9   | ✓      | 61498.4    | 15.75        | 10.97         |
| bare                     | 10.13.0 | ✗      | 59345.6    | 16.34        | 10.58         |
| foxify                   | 0.10.20 | ✓      | 59117.6    | 16.41        | 9.70          |
| polka                    | 0.5.2   | ✓      | 58537.6    | 16.59        | 10.44         |
| connect                  | 3.7.0   | ✗      | 57411.2    | 16.92        | 10.24         |
| micro                    | 9.4.1   | ✗      | 56088.0    | 17.33        | 10.00         |
| server-base              | 7.1.32  | ✗      | 55697.6    | 17.45        | 9.93          |
| fastify                  | 4.29.0  | ✓      | 55560.0    | 17.50        | 9.96          |
| server-base-router       | 7.1.32  | ✓      | 54194.4    | 17.95        | 9.66          |
| yeps                     | 1.1.1   | ✗      | 52480.8    | 18.56        | 9.36          |
| connect-router           | 1.3.8   | ✓      | 51241.6    | 19.02        | 9.14          |
| micro-route              | 2.5.0   | ✓      | 50447.2    | 19.32        | 9.00          |
| trek-engine              | 1.0.5   | ✗      | 48332.0    | 20.19        | 7.93          |
| trek-router              | 1.2.0   | ✓      | 47533.6    | 20.53        | 7.80          |
| vapr                     | 0.6.0   | ✓      | 45455.2    | 21.51        | 7.46          |
| yeps-router              | 1.2.0   | ✓      | 44032.0    | 22.22        | 7.85          |
| spirit                   | 0.6.1   | ✗      | 43579.2    | 22.44        | 7.77          |
| spirit-router            | 0.5.0   | ✓      | 43524.0    | 22.44        | 7.76          |
| koa                      | 2.16.0  | ✗      | 41654.4    | 23.51        | 7.43          |
| total.js                 | 3.4.13  | ✓      | 39848.0    | 24.60        | 12.20         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39527.0    | 24.79        | 7.05          |
| restify                  | 8.6.1   | ✓      | 39056.6    | 25.11        | 7.04          |
| take-five                | 2.0.0   | ✓      | 38469.4    | 25.50        | 13.83         |
| koa-router               | 12.0.1  | ✓      | 37105.8    | 26.45        | 6.62          |
| hapi                     | 20.3.0  | ✓      | 32669.4    | 30.10        | 5.83          |
| microrouter              | 3.1.3   | ✓      | 31649.4    | 31.09        | 5.64          |
| trpc-router              | 9.27.4  | ✓      | 27107.6    | 36.38        | 6.00          |
| egg.js                   | 3.30.1  | ✓      | 17709.5    | 55.94        | 6.33          |
| express                  | 4.21.2  | ✓      | 13591.0    | 73.06        | 2.42          |
| fastify-big-json         | 4.29.0  | ✓      | 12871.4    | 77.16        | 148.09        |
| express-with-middlewares | 4.21.2  | ✓      | 12469.8    | 79.65        | 4.64          |
| express-route-prefix     | 4.21.2  | ✓      | 11021.6    | 90.17        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

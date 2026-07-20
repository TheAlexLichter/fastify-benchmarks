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
* __Run:__ Mon Jul 20 2026 04:41:42 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 64590.8    | 14.99        | 11.52         |
| polkadot                 | 1.0.0   | ✗      | 64374.4    | 15.03        | 11.48         |
| h3                       | 0.8.6   | ✗      | 61914.4    | 15.66        | 10.16         |
| h3-router                | 0.8.6   | ✓      | 61687.2    | 15.72        | 10.12         |
| bare                     | 10.13.0 | ✗      | 57634.4    | 16.86        | 10.28         |
| restana                  | 4.9.9   | ✓      | 57427.2    | 16.92        | 10.24         |
| polka                    | 0.5.2   | ✓      | 57145.6    | 17.00        | 10.19         |
| foxify                   | 0.10.20 | ✓      | 57118.4    | 17.01        | 9.37          |
| micro                    | 9.4.1   | ✗      | 55271.2    | 17.60        | 9.86          |
| connect                  | 3.7.0   | ✗      | 54185.6    | 17.96        | 9.66          |
| fastify                  | 4.29.1  | ✓      | 53763.2    | 18.10        | 9.64          |
| server-base              | 7.1.32  | ✗      | 52633.6    | 18.50        | 9.39          |
| server-base-router       | 7.1.32  | ✓      | 52282.4    | 18.63        | 9.32          |
| yeps                     | 1.1.1   | ✗      | 49900.0    | 19.54        | 8.90          |
| connect-router           | 1.3.8   | ✓      | 48528.8    | 20.11        | 8.65          |
| micro-route              | 2.5.0   | ✓      | 48331.2    | 20.20        | 8.62          |
| trek-router              | 1.2.0   | ✓      | 45637.8    | 21.42        | 7.49          |
| trek-engine              | 1.0.5   | ✗      | 45452.6    | 21.51        | 7.46          |
| vapr                     | 0.6.0   | ✓      | 44826.4    | 21.81        | 7.35          |
| yeps-router              | 1.2.0   | ✓      | 42418.4    | 23.08        | 7.56          |
| spirit                   | 0.6.1   | ✗      | 41484.8    | 23.61        | 7.40          |
| spirit-router            | 0.5.0   | ✓      | 40631.2    | 24.12        | 7.25          |
| koa                      | 2.16.4  | ✗      | 39166.6    | 25.03        | 6.98          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37784.2    | 25.96        | 6.74          |
| take-five                | 2.0.0   | ✓      | 37712.6    | 26.01        | 13.56         |
| total.js                 | 3.4.13  | ✓      | 37369.8    | 26.26        | 11.44         |
| restify                  | 8.6.1   | ✓      | 37172.6    | 26.40        | 6.70          |
| koa-router               | 12.0.1  | ✓      | 34530.6    | 28.46        | 6.16          |
| hapi                     | 20.3.0  | ✓      | 31602.8    | 31.14        | 5.64          |
| microrouter              | 3.1.3   | ✓      | 30733.2    | 32.03        | 5.48          |
| trpc-router              | 9.27.4  | ✓      | 26218.0    | 37.64        | 5.80          |
| egg.js                   | 3.34.0  | ✓      | 17362.3    | 57.08        | 6.21          |
| express                  | 4.22.2  | ✓      | 12737.6    | 77.93        | 2.27          |
| fastify-big-json         | 4.29.1  | ✓      | 12203.6    | 81.40        | 140.41        |
| express-with-middlewares | 4.22.2  | ✓      | 11835.8    | 83.93        | 4.40          |
| express-route-prefix     | 4.22.2  | ✓      | 9791.5     | 101.52       | 3.62          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

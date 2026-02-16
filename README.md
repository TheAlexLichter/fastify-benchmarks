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
* __Run:__ Mon Feb 16 2026 03:43:11 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 81211.2    | 11.83        | 14.48         |
| 0http                    | 3.5.3   | ✓      | 80950.4    | 11.86        | 14.44         |
| bare                     | 10.13.0 | ✗      | 75656.4    | 12.72        | 13.49         |
| h3-router                | 0.8.6   | ✓      | 73731.6    | 13.07        | 12.09         |
| polka                    | 0.5.2   | ✓      | 73635.6    | 13.09        | 13.13         |
| foxify                   | 0.10.20 | ✓      | 73442.8    | 13.12        | 12.05         |
| restana                  | 4.9.9   | ✓      | 73278.8    | 13.15        | 13.07         |
| server-base              | 7.1.32  | ✗      | 72742.0    | 13.25        | 12.97         |
| h3                       | 0.8.6   | ✗      | 72291.6    | 13.34        | 11.86         |
| connect                  | 3.7.0   | ✗      | 71259.2    | 13.54        | 12.71         |
| server-base-router       | 7.1.32  | ✓      | 70345.2    | 13.72        | 12.55         |
| micro                    | 9.4.1   | ✗      | 70285.2    | 13.73        | 12.53         |
| fastify                  | 4.29.1  | ✓      | 69894.8    | 13.81        | 12.53         |
| yeps                     | 1.1.1   | ✗      | 68639.6    | 14.07        | 12.24         |
| micro-route              | 2.5.0   | ✓      | 66233.2    | 14.60        | 11.81         |
| connect-router           | 1.3.8   | ✓      | 65682.8    | 14.73        | 11.71         |
| trek-engine              | 1.0.5   | ✗      | 63552.0    | 15.24        | 10.42         |
| trek-router              | 1.2.0   | ✓      | 62246.4    | 15.57        | 10.21         |
| vapr                     | 0.6.0   | ✓      | 59568.8    | 16.29        | 9.77          |
| yeps-router              | 1.2.0   | ✓      | 54916.0    | 17.71        | 9.79          |
| koa                      | 2.16.3  | ✗      | 53776.8    | 18.10        | 9.59          |
| spirit                   | 0.6.1   | ✗      | 53224.8    | 18.29        | 9.49          |
| total.js                 | 3.4.13  | ✓      | 52355.2    | 18.60        | 16.03         |
| take-five                | 2.0.0   | ✓      | 52214.4    | 18.65        | 18.77         |
| spirit-router            | 0.5.0   | ✓      | 51610.4    | 18.89        | 9.20          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 49737.6    | 19.61        | 8.87          |
| restify                  | 8.6.1   | ✓      | 48558.4    | 20.10        | 8.75          |
| koa-router               | 12.0.1  | ✓      | 46639.2    | 20.94        | 8.32          |
| hapi                     | 20.3.0  | ✓      | 40322.2    | 24.30        | 7.19          |
| microrouter              | 3.1.3   | ✓      | 39788.8    | 24.63        | 7.10          |
| trpc-router              | 9.27.4  | ✓      | 33277.2    | 29.55        | 7.36          |
| egg.js                   | 3.34.0  | ✓      | 18841.7    | 52.56        | 6.74          |
| express                  | 4.22.1  | ✓      | 15665.1    | 63.31        | 2.79          |
| express-with-middlewares | 4.22.1  | ✓      | 14938.6    | 66.40        | 5.56          |
| fastify-big-json         | 4.29.1  | ✓      | 13008.6    | 76.33        | 149.67        |
| express-route-prefix     | 4.22.1  | ✓      | 11978.2    | 82.92        | 4.43          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Jul 21 2025 03:19:10 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 70908.4    | 13.61        | 12.65         |
| 0http                    | 3.5.3   | ✓      | 69473.2    | 13.90        | 12.39         |
| h3                       | 0.8.6   | ✗      | 68830.8    | 14.04        | 11.29         |
| h3-router                | 0.8.6   | ✓      | 65390.8    | 14.80        | 10.73         |
| restana                  | 4.9.9   | ✓      | 63585.6    | 15.24        | 11.34         |
| bare                     | 10.13.0 | ✗      | 61395.2    | 15.80        | 10.95         |
| foxify                   | 0.10.20 | ✓      | 59848.0    | 16.21        | 9.82          |
| polka                    | 0.5.2   | ✓      | 59247.2    | 16.37        | 10.57         |
| connect                  | 3.7.0   | ✗      | 58521.6    | 16.58        | 10.44         |
| micro                    | 9.4.1   | ✗      | 58441.6    | 16.62        | 10.42         |
| fastify                  | 4.29.1  | ✓      | 56942.4    | 17.06        | 10.21         |
| server-base-router       | 7.1.32  | ✓      | 56206.4    | 17.30        | 10.02         |
| server-base              | 7.1.32  | ✗      | 56107.2    | 17.33        | 10.01         |
| yeps                     | 1.1.1   | ✗      | 53496.8    | 18.20        | 9.54          |
| connect-router           | 1.3.8   | ✓      | 51931.2    | 18.76        | 9.26          |
| micro-route              | 2.5.0   | ✓      | 50912.8    | 19.15        | 9.08          |
| trek-engine              | 1.0.5   | ✗      | 49295.2    | 19.79        | 8.09          |
| trek-router              | 1.2.0   | ✓      | 48769.6    | 20.01        | 8.00          |
| vapr                     | 0.6.0   | ✓      | 47372.0    | 20.62        | 7.77          |
| spirit                   | 0.6.1   | ✗      | 46720.0    | 20.92        | 8.33          |
| yeps-router              | 1.2.0   | ✓      | 44243.2    | 22.10        | 7.89          |
| spirit-router            | 0.5.0   | ✓      | 44183.2    | 22.14        | 7.88          |
| koa                      | 2.16.1  | ✗      | 43119.2    | 22.67        | 7.69          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40915.8    | 23.92        | 7.30          |
| total.js                 | 3.4.13  | ✓      | 40359.0    | 24.28        | 12.35         |
| restify                  | 8.6.1   | ✓      | 39833.6    | 24.63        | 7.18          |
| take-five                | 2.0.0   | ✓      | 39733.8    | 24.67        | 14.29         |
| koa-router               | 12.0.1  | ✓      | 37195.0    | 26.38        | 6.63          |
| hapi                     | 20.3.0  | ✓      | 34353.8    | 28.60        | 6.13          |
| microrouter              | 3.1.3   | ✓      | 32309.0    | 30.45        | 5.76          |
| trpc-router              | 9.27.4  | ✓      | 27648.0    | 35.66        | 6.12          |
| egg.js                   | 3.31.0  | ✓      | 17375.0    | 57.02        | 6.21          |
| express                  | 4.21.2  | ✓      | 13723.0    | 72.33        | 2.45          |
| fastify-big-json         | 4.29.1  | ✓      | 12816.8    | 77.48        | 147.47        |
| express-with-middlewares | 4.21.2  | ✓      | 12379.6    | 80.23        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 11065.2    | 89.80        | 4.09          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

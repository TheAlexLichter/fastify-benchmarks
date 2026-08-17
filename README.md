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
* __Run:__ Mon Aug 17 2026 02:37:00 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 62217.6    | 15.58        | 11.10         |
| polkadot                 | 1.0.0   | ✗      | 61077.6    | 15.87        | 10.89         |
| h3                       | 0.8.6   | ✗      | 60596.8    | 16.01        | 9.94          |
| restana                  | 4.9.9   | ✓      | 57774.4    | 16.82        | 10.30         |
| h3-router                | 0.8.6   | ✓      | 57637.6    | 16.85        | 9.45          |
| bare                     | 10.13.0 | ✗      | 57472.0    | 16.90        | 10.25         |
| polka                    | 0.5.2   | ✓      | 56608.8    | 17.17        | 10.09         |
| foxify                   | 0.10.20 | ✓      | 56317.6    | 17.26        | 9.24          |
| connect                  | 3.7.0   | ✗      | 54647.2    | 17.80        | 9.75          |
| fastify                  | 4.29.1  | ✓      | 54050.4    | 18.00        | 9.69          |
| micro                    | 9.4.1   | ✗      | 53774.4    | 18.10        | 9.59          |
| server-base              | 7.1.32  | ✗      | 53026.4    | 18.36        | 9.46          |
| server-base-router       | 7.1.32  | ✓      | 52832.8    | 18.43        | 9.42          |
| yeps                     | 1.1.1   | ✗      | 49862.4    | 19.56        | 8.89          |
| micro-route              | 2.5.0   | ✓      | 49106.4    | 19.87        | 8.76          |
| connect-router           | 1.3.8   | ✓      | 49078.4    | 19.88        | 8.75          |
| trek-engine              | 1.0.5   | ✗      | 46992.6    | 20.78        | 7.71          |
| trek-router              | 1.2.0   | ✓      | 45750.4    | 21.36        | 7.50          |
| vapr                     | 0.6.0   | ✓      | 45080.8    | 21.69        | 7.39          |
| yeps-router              | 1.2.0   | ✓      | 41854.4    | 23.39        | 7.46          |
| koa                      | 2.16.4  | ✗      | 41161.8    | 23.80        | 7.34          |
| spirit-router            | 0.5.0   | ✓      | 40724.0    | 24.06        | 7.26          |
| spirit                   | 0.6.1   | ✗      | 40496.0    | 24.20        | 7.22          |
| total.js                 | 3.4.13  | ✓      | 37919.0    | 25.87        | 11.61         |
| take-five                | 2.0.0   | ✓      | 37743.8    | 25.99        | 13.57         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37676.2    | 26.04        | 6.72          |
| restify                  | 8.6.1   | ✓      | 36919.0    | 26.59        | 6.65          |
| koa-router               | 12.0.1  | ✓      | 34457.4    | 28.52        | 6.14          |
| hapi                     | 20.3.0  | ✓      | 31445.0    | 31.30        | 5.61          |
| microrouter              | 3.1.3   | ✓      | 30639.2    | 32.13        | 5.46          |
| trpc-router              | 9.27.4  | ✓      | 26727.2    | 36.91        | 5.91          |
| egg.js                   | 3.34.0  | ✓      | 16766.9    | 59.13        | 6.00          |
| express                  | 4.22.2  | ✓      | 12945.6    | 76.69        | 2.31          |
| fastify-big-json         | 4.29.1  | ✓      | 12088.8    | 82.16        | 139.09        |
| express-with-middlewares | 4.22.2  | ✓      | 11821.1    | 84.03        | 4.40          |
| express-route-prefix     | 4.22.2  | ✓      | 10154.8    | 97.86        | 3.76          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

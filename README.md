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
* __Run:__ Mon Jan 26 2026 03:23:57 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 78267.2    | 12.28        | 13.96         |
| polkadot                 | 1.0.0   | ✗      | 77524.8    | 12.41        | 13.83         |
| foxify                   | 0.10.20 | ✓      | 72969.6    | 13.21        | 11.97         |
| bare                     | 10.13.0 | ✗      | 72305.6    | 13.34        | 12.89         |
| h3-router                | 0.8.6   | ✓      | 72124.8    | 13.37        | 11.83         |
| polka                    | 0.5.2   | ✓      | 71714.0    | 13.45        | 12.79         |
| h3                       | 0.8.6   | ✗      | 71481.2    | 13.50        | 11.73         |
| connect                  | 3.7.0   | ✗      | 70868.4    | 13.61        | 12.64         |
| restana                  | 4.9.9   | ✓      | 70633.6    | 13.66        | 12.60         |
| micro                    | 9.4.1   | ✗      | 69422.4    | 13.91        | 12.38         |
| fastify                  | 4.29.1  | ✓      | 69256.0    | 13.94        | 12.42         |
| server-base-router       | 7.1.32  | ✓      | 66643.2    | 14.51        | 11.89         |
| yeps                     | 1.1.1   | ✗      | 65604.8    | 14.74        | 11.70         |
| server-base              | 7.1.32  | ✗      | 65151.6    | 14.85        | 11.62         |
| micro-route              | 2.5.0   | ✓      | 64023.2    | 15.12        | 11.42         |
| connect-router           | 1.3.8   | ✓      | 62144.8    | 15.59        | 11.08         |
| trek-router              | 1.2.0   | ✓      | 59033.6    | 16.44        | 9.68          |
| trek-engine              | 1.0.5   | ✗      | 57557.6    | 16.88        | 9.44          |
| vapr                     | 0.6.0   | ✓      | 56623.2    | 17.16        | 9.29          |
| yeps-router              | 1.2.0   | ✓      | 53326.4    | 18.25        | 9.51          |
| koa                      | 2.16.3  | ✗      | 51840.0    | 18.79        | 9.25          |
| take-five                | 2.0.0   | ✓      | 48871.2    | 19.96        | 17.57         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 48711.2    | 20.03        | 8.69          |
| spirit                   | 0.6.1   | ✗      | 47748.0    | 20.44        | 8.51          |
| total.js                 | 3.4.13  | ✓      | 46478.4    | 21.02        | 14.23         |
| restify                  | 8.6.1   | ✓      | 46080.0    | 21.20        | 8.31          |
| spirit-router            | 0.5.0   | ✓      | 45770.4    | 21.35        | 8.16          |
| koa-router               | 12.0.1  | ✓      | 44916.0    | 21.77        | 8.01          |
| hapi                     | 20.3.0  | ✓      | 38791.8    | 25.28        | 6.92          |
| microrouter              | 3.1.3   | ✓      | 37136.2    | 26.43        | 6.62          |
| trpc-router              | 9.27.4  | ✓      | 31646.2    | 31.10        | 7.00          |
| egg.js                   | 3.34.0  | ✓      | 18781.1    | 52.73        | 6.72          |
| express                  | 4.22.1  | ✓      | 15623.4    | 63.47        | 2.79          |
| express-with-middlewares | 4.22.1  | ✓      | 14505.0    | 68.40        | 5.39          |
| fastify-big-json         | 4.29.1  | ✓      | 13051.6    | 76.07        | 150.17        |
| express-route-prefix     | 4.22.1  | ✓      | 12094.4    | 82.13        | 4.48          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

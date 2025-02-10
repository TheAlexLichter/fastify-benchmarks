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
* __Run:__ Mon Feb 10 2025 02:38:53 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69846.0    | 13.81        | 12.46         |
| 0http                    | 3.5.3   | ✓      | 66994.0    | 14.44        | 11.95         |
| h3                       | 0.8.6   | ✗      | 64938.8    | 14.90        | 10.65         |
| h3-router                | 0.8.6   | ✓      | 62734.4    | 15.44        | 10.29         |
| restana                  | 4.9.9   | ✓      | 61250.4    | 15.83        | 10.92         |
| bare                     | 10.13.0 | ✗      | 60508.0    | 16.03        | 10.79         |
| polka                    | 0.5.2   | ✓      | 58546.4    | 16.58        | 10.44         |
| foxify                   | 0.10.20 | ✓      | 57504.0    | 16.89        | 9.43          |
| fastify                  | 4.29.0  | ✓      | 57076.8    | 17.03        | 10.23         |
| connect                  | 3.7.0   | ✗      | 56550.4    | 17.19        | 10.08         |
| micro                    | 9.4.1   | ✗      | 56256.0    | 17.28        | 10.03         |
| server-base-router       | 7.1.32  | ✓      | 54292.0    | 17.93        | 9.68          |
| server-base              | 7.1.32  | ✗      | 54229.6    | 17.95        | 9.67          |
| yeps                     | 1.1.1   | ✗      | 54096.8    | 18.00        | 9.65          |
| connect-router           | 1.3.8   | ✓      | 50512.0    | 19.30        | 9.01          |
| micro-route              | 2.5.0   | ✓      | 49951.2    | 19.52        | 8.91          |
| trek-engine              | 1.0.5   | ✗      | 48886.4    | 19.95        | 8.02          |
| trek-router              | 1.2.0   | ✓      | 48439.2    | 20.15        | 7.95          |
| vapr                     | 0.6.0   | ✓      | 46212.0    | 21.14        | 7.58          |
| spirit                   | 0.6.1   | ✗      | 44855.2    | 21.84        | 8.00          |
| yeps-router              | 1.2.0   | ✓      | 44172.8    | 22.13        | 7.88          |
| spirit-router            | 0.5.0   | ✓      | 42280.8    | 23.13        | 7.54          |
| koa                      | 2.15.3  | ✗      | 41995.2    | 23.32        | 7.49          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40383.4    | 24.26        | 7.20          |
| total.js                 | 3.4.13  | ✓      | 39797.6    | 24.62        | 12.18         |
| restify                  | 8.6.1   | ✓      | 39783.0    | 24.62        | 7.17          |
| take-five                | 2.0.0   | ✓      | 39775.8    | 24.65        | 14.30         |
| koa-router               | 12.0.1  | ✓      | 38077.8    | 25.77        | 6.79          |
| hapi                     | 20.3.0  | ✓      | 34103.2    | 28.81        | 6.08          |
| microrouter              | 3.1.3   | ✓      | 32166.6    | 30.58        | 5.74          |
| trpc-router              | 9.27.4  | ✓      | 27869.2    | 35.37        | 6.17          |
| egg.js                   | 3.30.1  | ✓      | 17131.3    | 57.86        | 6.13          |
| express                  | 4.21.2  | ✓      | 13849.6    | 71.65        | 2.47          |
| fastify-big-json         | 4.29.0  | ✓      | 12713.0    | 78.12        | 146.28        |
| express-with-middlewares | 4.21.2  | ✓      | 12486.6    | 79.52        | 4.64          |
| express-route-prefix     | 4.21.2  | ✓      | 11022.0    | 90.15        | 4.08          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

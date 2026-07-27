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
* __Run:__ Mon Jul 27 2026 04:42:17 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66829.2    | 14.46        | 11.92         |
| polkadot                 | 1.0.0   | ✗      | 64527.2    | 15.01        | 11.51         |
| h3                       | 0.8.6   | ✗      | 64284.8    | 15.07        | 10.54         |
| h3-router                | 0.8.6   | ✓      | 61636.8    | 15.73        | 10.11         |
| bare                     | 10.13.0 | ✗      | 60504.0    | 16.03        | 10.79         |
| restana                  | 4.9.9   | ✓      | 59992.8    | 16.16        | 10.70         |
| foxify                   | 0.10.20 | ✓      | 59169.6    | 16.41        | 9.70          |
| connect                  | 3.7.0   | ✗      | 58620.0    | 16.56        | 10.45         |
| polka                    | 0.5.2   | ✓      | 57651.2    | 16.85        | 10.28         |
| micro                    | 9.4.1   | ✗      | 57243.2    | 16.98        | 10.21         |
| fastify                  | 4.29.1  | ✓      | 56313.6    | 17.26        | 10.10         |
| server-base              | 7.1.32  | ✗      | 55857.6    | 17.41        | 9.96          |
| server-base-router       | 7.1.32  | ✓      | 54696.8    | 17.79        | 9.75          |
| yeps                     | 1.1.1   | ✗      | 54052.0    | 18.00        | 9.64          |
| connect-router           | 1.3.8   | ✓      | 52151.2    | 18.68        | 9.30          |
| micro-route              | 2.5.0   | ✓      | 50253.6    | 19.40        | 8.96          |
| trek-router              | 1.2.0   | ✓      | 47985.6    | 20.34        | 7.87          |
| trek-engine              | 1.0.5   | ✗      | 47977.6    | 20.35        | 7.87          |
| vapr                     | 0.6.0   | ✓      | 45948.0    | 21.27        | 7.54          |
| yeps-router              | 1.2.0   | ✓      | 43502.4    | 22.48        | 7.76          |
| koa                      | 2.16.4  | ✗      | 42088.0    | 23.26        | 7.51          |
| spirit-router            | 0.5.0   | ✓      | 42018.4    | 23.30        | 7.49          |
| spirit                   | 0.6.1   | ✗      | 40626.4    | 24.11        | 7.24          |
| total.js                 | 3.4.13  | ✓      | 39105.0    | 25.07        | 11.97         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38555.8    | 25.44        | 6.88          |
| restify                  | 8.6.1   | ✓      | 38270.4    | 25.63        | 6.90          |
| take-five                | 2.0.0   | ✓      | 38183.8    | 25.69        | 13.73         |
| koa-router               | 12.0.1  | ✓      | 36249.0    | 27.08        | 6.46          |
| hapi                     | 20.3.0  | ✓      | 31888.6    | 30.86        | 5.69          |
| microrouter              | 3.1.3   | ✓      | 31567.6    | 31.18        | 5.63          |
| trpc-router              | 9.27.4  | ✓      | 26925.6    | 36.64        | 5.96          |
| egg.js                   | 3.34.0  | ✓      | 16846.6    | 58.82        | 6.02          |
| express                  | 4.22.2  | ✓      | 13163.8    | 75.41        | 2.35          |
| express-with-middlewares | 4.22.2  | ✓      | 12704.2    | 78.17        | 4.72          |
| fastify-big-json         | 4.29.1  | ✓      | 12361.0    | 80.35        | 142.23        |
| express-route-prefix     | 4.22.2  | ✓      | 10136.5    | 98.09        | 3.75          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

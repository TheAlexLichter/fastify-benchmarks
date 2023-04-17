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

* __Machine:__ linux x64 | 2 vCPUs | 6.8GB Mem
* __Node:__ `v14.21.3`
* __Run:__ Mon Apr 17 2023 02:24:43 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| fastify                  | 4.15.0  | ✓      | 47347.2    | 20.63        | 8.49          |
| bare                     | 10.13.0 | ✗      | 47180.8    | 20.73        | 8.41          |
| foxify                   | 0.10.20 | ✓      | 46768.0    | 20.88        | 7.67          |
| micro                    | 9.4.1   | ✗      | 46664.0    | 20.94        | 8.32          |
| server-base              | 7.1.32  | ✗      | 46554.4    | 20.99        | 8.30          |
| polka                    | 0.5.2   | ✓      | 46072.8    | 21.21        | 8.22          |
| polkadot                 | 1.0.0   | ✗      | 45298.4    | 21.58        | 8.08          |
| 0http                    | 3.5.1   | ✓      | 45132.6    | 21.67        | 8.05          |
| connect                  | 3.7.0   | ✗      | 44902.6    | 21.78        | 8.01          |
| server-base-router       | 7.1.32  | ✓      | 44543.0    | 21.96        | 7.94          |
| h3                       | 0.8.6   | ✗      | 44494.6    | 22.00        | 7.30          |
| yeps                     | 1.1.1   | ✗      | 43918.4    | 22.27        | 7.83          |
| h3-router                | 0.8.6   | ✓      | 42580.0    | 23.01        | 6.98          |
| connect-router           | 1.3.8   | ✓      | 42132.0    | 23.28        | 7.51          |
| restana                  | 4.9.7   | ✓      | 41410.6    | 23.65        | 7.39          |
| trek-engine              | 1.0.5   | ✗      | 40209.4    | 24.38        | 6.60          |
| micro-route              | 2.5.0   | ✓      | 40131.4    | 24.43        | 7.16          |
| trek-router              | 1.2.0   | ✓      | 38703.8    | 25.34        | 6.35          |
| vapr                     | 0.6.0   | ✓      | 36635.8    | 26.80        | 6.01          |
| yeps-router              | 1.2.0   | ✓      | 35952.2    | 27.32        | 6.41          |
| koa                      | 2.14.2  | ✗      | 35461.4    | 27.70        | 6.32          |
| spirit                   | 0.6.1   | ✗      | 33775.2    | 29.14        | 6.02          |
| spirit-router            | 0.5.0   | ✓      | 33342.0    | 29.53        | 5.95          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 32296.0    | 30.46        | 5.76          |
| take-five                | 2.0.0   | ✓      | 32179.0    | 30.57        | 11.57         |
| total.js                 | 3.4.13  | ✓      | 31432.6    | 31.31        | 9.62          |
| restify                  | 8.6.1   | ✓      | 30972.0    | 31.79        | 5.58          |
| koa-router               | 12.0.0  | ✓      | 29818.4    | 33.06        | 5.32          |
| hapi                     | 20.3.0  | ✓      | 26654.0    | 37.03        | 4.75          |
| microrouter              | 3.1.3   | ✓      | 25216.8    | 39.15        | 4.50          |
| trpc-router              | 9.27.3  | ✓      | 20122.3    | 49.19        | 4.45          |
| egg.js                   | 3.15.0  | ✓      | 13120.2    | 75.69        | 4.69          |
| express                  | 4.18.2  | ✓      | 10071.3    | 98.77        | 1.80          |
| express-with-middlewares | 4.18.2  | ✓      | 8910.5     | 111.61       | 3.31          |
| fastify-big-json         | 4.15.0  | ✓      | 8344.5     | 119.35       | 96.01         |
| express-route-prefix     | 4.18.2  | ✓      | 7311.9     | 136.15       | 2.71          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

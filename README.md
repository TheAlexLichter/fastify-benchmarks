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
* __Run:__ Mon Mar 18 2024 02:07:15 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 64409.6    | 15.02        | 11.49         |
| 0http                    | 3.5.2   | ✓      | 62752.0    | 15.44        | 11.19         |
| h3                       | 0.8.6   | ✗      | 62444.4    | 15.52        | 10.24         |
| h3-router                | 0.8.6   | ✓      | 62100.0    | 15.61        | 10.19         |
| bare                     | 10.13.0 | ✗      | 58787.2    | 16.51        | 10.48         |
| polka                    | 0.5.2   | ✓      | 57764.0    | 16.82        | 10.30         |
| foxify                   | 0.10.20 | ✓      | 56963.2    | 17.06        | 9.34          |
| micro                    | 9.4.1   | ✗      | 56108.0    | 17.33        | 10.01         |
| connect                  | 3.7.0   | ✗      | 55667.2    | 17.47        | 9.93          |
| restana                  | 4.9.7   | ✓      | 55324.8    | 17.57        | 9.87          |
| server-base-router       | 7.1.32  | ✓      | 54435.2    | 17.87        | 9.71          |
| fastify                  | 4.26.2  | ✓      | 54172.8    | 17.96        | 9.71          |
| server-base              | 7.1.32  | ✗      | 53822.4    | 18.09        | 9.60          |
| yeps                     | 1.1.1   | ✗      | 52648.8    | 18.49        | 9.39          |
| connect-router           | 1.3.8   | ✓      | 50042.4    | 19.49        | 8.92          |
| micro-route              | 2.5.0   | ✓      | 49519.2    | 19.69        | 8.83          |
| trek-engine              | 1.0.5   | ✗      | 48944.8    | 19.94        | 8.03          |
| trek-router              | 1.2.0   | ✓      | 47910.4    | 20.37        | 7.86          |
| vapr                     | 0.6.0   | ✓      | 45806.4    | 21.33        | 7.51          |
| yeps-router              | 1.2.0   | ✓      | 44512.8    | 21.98        | 7.94          |
| spirit                   | 0.6.1   | ✗      | 42165.6    | 23.21        | 7.52          |
| koa                      | 2.15.1  | ✗      | 41979.2    | 23.32        | 7.49          |
| spirit-router            | 0.5.0   | ✓      | 41232.0    | 23.76        | 7.35          |
| total.js                 | 3.4.13  | ✓      | 39018.4    | 25.13        | 11.95         |
| take-five                | 2.0.0   | ✓      | 38907.4    | 25.20        | 13.99         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38721.0    | 25.33        | 6.91          |
| restify                  | 8.6.1   | ✓      | 38507.4    | 25.46        | 6.94          |
| koa-router               | 12.0.1  | ✓      | 37375.8    | 26.26        | 6.67          |
| hapi                     | 20.3.0  | ✓      | 32554.8    | 30.21        | 5.81          |
| microrouter              | 3.1.3   | ✓      | 31717.8    | 31.03        | 5.66          |
| trpc-router              | 9.27.4  | ✓      | 26407.2    | 37.37        | 5.84          |
| egg.js                   | 3.20.0  | ✓      | 17273.7    | 57.38        | 6.18          |
| express                  | 4.18.3  | ✓      | 13721.2    | 72.32        | 2.45          |
| fastify-big-json         | 4.26.2  | ✓      | 12844.4    | 77.32        | 147.79        |
| express-with-middlewares | 4.18.3  | ✓      | 12652.6    | 78.48        | 4.71          |
| express-route-prefix     | 4.18.3  | ✓      | 10947.6    | 90.76        | 4.05          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

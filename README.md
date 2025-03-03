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
* __Run:__ Mon Mar 03 2025 02:44:19 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69086.0    | 13.98        | 12.32         |
| 0http                    | 3.5.3   | ✓      | 66985.2    | 14.43        | 11.95         |
| h3                       | 0.8.6   | ✗      | 65604.8    | 14.74        | 10.76         |
| h3-router                | 0.8.6   | ✓      | 65419.6    | 14.80        | 10.73         |
| restana                  | 4.9.9   | ✓      | 60433.6    | 16.08        | 10.78         |
| bare                     | 10.13.0 | ✗      | 59038.4    | 16.44        | 10.53         |
| polka                    | 0.5.2   | ✓      | 59028.8    | 16.43        | 10.53         |
| foxify                   | 0.10.20 | ✓      | 58541.6    | 16.57        | 9.60          |
| micro                    | 9.4.1   | ✗      | 56552.8    | 17.19        | 10.09         |
| connect                  | 3.7.0   | ✗      | 55531.2    | 17.51        | 9.90          |
| server-base-router       | 7.1.32  | ✓      | 55122.4    | 17.64        | 9.83          |
| fastify                  | 4.29.0  | ✓      | 55002.4    | 17.68        | 9.86          |
| server-base              | 7.1.32  | ✗      | 53717.6    | 18.12        | 9.58          |
| yeps                     | 1.1.1   | ✗      | 51268.0    | 19.02        | 9.14          |
| micro-route              | 2.5.0   | ✓      | 50940.0    | 19.15        | 9.08          |
| connect-router           | 1.3.8   | ✓      | 50535.2    | 19.29        | 9.01          |
| trek-engine              | 1.0.5   | ✗      | 48696.8    | 20.03        | 7.99          |
| trek-router              | 1.2.0   | ✓      | 47464.0    | 20.57        | 7.79          |
| vapr                     | 0.6.0   | ✓      | 46306.4    | 21.10        | 7.60          |
| spirit-router            | 0.5.0   | ✓      | 44182.4    | 22.12        | 7.88          |
| yeps-router              | 1.2.0   | ✓      | 43903.2    | 22.28        | 7.83          |
| koa                      | 2.16.0  | ✗      | 42418.4    | 23.07        | 7.56          |
| spirit                   | 0.6.1   | ✗      | 41398.4    | 23.66        | 7.38          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40512.0    | 24.18        | 7.22          |
| total.js                 | 3.4.13  | ✓      | 39166.6    | 25.04        | 11.99         |
| take-five                | 2.0.0   | ✓      | 39053.0    | 25.10        | 14.04         |
| restify                  | 8.6.1   | ✓      | 38656.6    | 25.37        | 6.97          |
| koa-router               | 12.0.1  | ✓      | 37154.6    | 26.43        | 6.63          |
| hapi                     | 20.3.0  | ✓      | 33682.6    | 29.17        | 6.01          |
| microrouter              | 3.1.3   | ✓      | 31369.6    | 31.38        | 5.59          |
| trpc-router              | 9.27.4  | ✓      | 27206.8    | 36.25        | 6.02          |
| egg.js                   | 3.30.1  | ✓      | 17212.6    | 57.57        | 6.16          |
| express                  | 4.21.2  | ✓      | 13526.0    | 73.39        | 2.41          |
| fastify-big-json         | 4.29.0  | ✓      | 12765.4    | 77.80        | 146.87        |
| express-with-middlewares | 4.21.2  | ✓      | 12512.2    | 79.37        | 4.65          |
| express-route-prefix     | 4.21.2  | ✓      | 10858.2    | 91.51        | 4.02          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

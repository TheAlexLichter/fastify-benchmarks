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
* __Run:__ Mon Feb 17 2025 02:41:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69120.8    | 13.97        | 12.33         |
| 0http                    | 3.5.3   | ✓      | 68821.2    | 14.04        | 12.27         |
| h3                       | 0.8.6   | ✗      | 65710.8    | 14.72        | 10.78         |
| restana                  | 4.9.9   | ✓      | 61814.4    | 15.68        | 11.02         |
| h3-router                | 0.8.6   | ✓      | 60802.4    | 15.95        | 9.97          |
| bare                     | 10.13.0 | ✗      | 60787.2    | 15.97        | 10.84         |
| foxify                   | 0.10.20 | ✓      | 58926.4    | 16.47        | 9.67          |
| polka                    | 0.5.2   | ✓      | 58472.0    | 16.61        | 10.43         |
| connect                  | 3.7.0   | ✗      | 57394.4    | 16.93        | 10.23         |
| micro                    | 9.4.1   | ✗      | 56923.2    | 17.07        | 10.15         |
| fastify                  | 4.29.0  | ✓      | 56424.8    | 17.23        | 10.12         |
| server-base-router       | 7.1.32  | ✓      | 55080.0    | 17.66        | 9.82          |
| server-base              | 7.1.32  | ✗      | 54436.8    | 17.87        | 9.71          |
| yeps                     | 1.1.1   | ✗      | 53225.6    | 18.29        | 9.49          |
| connect-router           | 1.3.8   | ✓      | 49908.8    | 19.55        | 8.90          |
| micro-route              | 2.5.0   | ✓      | 49652.0    | 19.64        | 8.85          |
| trek-engine              | 1.0.5   | ✗      | 48384.8    | 20.17        | 7.94          |
| trek-router              | 1.2.0   | ✓      | 47776.8    | 20.43        | 7.84          |
| vapr                     | 0.6.0   | ✓      | 46183.2    | 21.15        | 7.58          |
| spirit                   | 0.6.1   | ✗      | 44542.4    | 21.95        | 7.94          |
| yeps-router              | 1.2.0   | ✓      | 44133.6    | 22.15        | 7.87          |
| spirit-router            | 0.5.0   | ✓      | 43865.6    | 22.28        | 7.82          |
| koa                      | 2.15.4  | ✗      | 42496.8    | 23.03        | 7.58          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39366.2    | 24.90        | 7.02          |
| take-five                | 2.0.0   | ✓      | 39122.2    | 25.06        | 14.07         |
| total.js                 | 3.4.13  | ✓      | 38901.6    | 25.21        | 11.91         |
| restify                  | 8.6.1   | ✓      | 38523.8    | 25.46        | 6.94          |
| koa-router               | 12.0.1  | ✓      | 36815.0    | 26.66        | 6.57          |
| hapi                     | 20.3.0  | ✓      | 33704.8    | 29.17        | 6.01          |
| microrouter              | 3.1.3   | ✓      | 32126.4    | 30.62        | 5.73          |
| trpc-router              | 9.27.4  | ✓      | 26694.0    | 36.95        | 5.91          |
| egg.js                   | 3.30.1  | ✓      | 17576.2    | 56.36        | 6.29          |
| express                  | 4.21.2  | ✓      | 13415.4    | 74.00        | 2.39          |
| fastify-big-json         | 4.29.0  | ✓      | 12831.6    | 77.38        | 147.62        |
| express-with-middlewares | 4.21.2  | ✓      | 12376.8    | 80.23        | 4.60          |
| express-route-prefix     | 4.21.2  | ✓      | 10985.5    | 90.45        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

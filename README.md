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
* __Run:__ Mon May 06 2024 02:11:44 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68520.0    | 14.10        | 12.22         |
| polkadot                 | 1.0.0   | ✗      | 65858.8    | 14.69        | 11.75         |
| h3                       | 0.8.6   | ✗      | 64464.8    | 15.02        | 10.58         |
| h3-router                | 0.8.6   | ✓      | 61500.8    | 15.77        | 10.09         |
| bare                     | 10.13.0 | ✗      | 59317.6    | 16.35        | 10.58         |
| foxify                   | 0.10.20 | ✓      | 57835.2    | 16.80        | 9.49          |
| polka                    | 0.5.2   | ✓      | 56530.4    | 17.19        | 10.08         |
| restana                  | 4.9.9   | ✓      | 56360.8    | 17.25        | 10.05         |
| connect                  | 3.7.0   | ✗      | 56152.8    | 17.32        | 10.01         |
| fastify                  | 4.26.2  | ✓      | 55402.4    | 17.55        | 9.93          |
| micro                    | 9.4.1   | ✗      | 54664.8    | 17.80        | 9.75          |
| server-base              | 7.1.32  | ✗      | 52764.0    | 18.45        | 9.41          |
| server-base-router       | 7.1.32  | ✓      | 51918.4    | 18.77        | 9.26          |
| yeps                     | 1.1.1   | ✗      | 51635.2    | 18.87        | 9.21          |
| micro-route              | 2.5.0   | ✓      | 49530.4    | 19.70        | 8.83          |
| connect-router           | 1.3.8   | ✓      | 48391.2    | 20.16        | 8.63          |
| trek-engine              | 1.0.5   | ✗      | 47740.8    | 20.45        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 47148.0    | 20.71        | 7.73          |
| vapr                     | 0.6.0   | ✓      | 45730.4    | 21.37        | 7.50          |
| spirit                   | 0.6.1   | ✗      | 43791.2    | 22.37        | 7.81          |
| yeps-router              | 1.2.0   | ✓      | 43686.4    | 22.39        | 7.79          |
| spirit-router            | 0.5.0   | ✓      | 41776.0    | 23.43        | 7.45          |
| koa                      | 2.15.3  | ✗      | 41123.4    | 23.82        | 7.33          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39522.6    | 24.80        | 7.05          |
| total.js                 | 3.4.13  | ✓      | 39112.0    | 25.07        | 11.97         |
| take-five                | 2.0.0   | ✓      | 38377.8    | 25.56        | 13.80         |
| restify                  | 8.6.1   | ✓      | 37749.0    | 25.98        | 6.80          |
| koa-router               | 12.0.1  | ✓      | 36603.4    | 26.82        | 6.53          |
| hapi                     | 20.3.0  | ✓      | 33668.8    | 29.20        | 6.00          |
| microrouter              | 3.1.3   | ✓      | 32427.0    | 30.33        | 5.78          |
| trpc-router              | 9.27.4  | ✓      | 26432.8    | 37.33        | 5.85          |
| egg.js                   | 3.22.0  | ✓      | 17286.2    | 57.32        | 6.18          |
| express                  | 4.19.2  | ✓      | 13828.0    | 71.77        | 2.47          |
| fastify-big-json         | 4.26.2  | ✓      | 13043.0    | 76.11        | 150.07        |
| express-with-middlewares | 4.19.2  | ✓      | 12180.4    | 81.54        | 4.53          |
| express-route-prefix     | 4.19.2  | ✓      | 10749.5    | 92.46        | 3.98          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

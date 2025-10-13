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
* __Run:__ Mon Oct 13 2025 02:53:25 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 71201.2    | 13.55        | 12.70         |
| 0http                    | 3.5.3   | ✓      | 68750.0    | 14.05        | 12.26         |
| h3                       | 0.8.6   | ✗      | 61718.4    | 15.70        | 10.12         |
| h3-router                | 0.8.6   | ✓      | 61170.4    | 15.86        | 10.03         |
| bare                     | 10.13.0 | ✗      | 61114.4    | 15.87        | 10.90         |
| restana                  | 4.9.9   | ✓      | 61042.4    | 15.92        | 10.89         |
| foxify                   | 0.10.20 | ✓      | 57426.4    | 16.92        | 9.42          |
| polka                    | 0.5.2   | ✓      | 56904.0    | 17.07        | 10.15         |
| connect                  | 3.7.0   | ✗      | 56615.2    | 17.16        | 10.10         |
| server-base-router       | 7.1.32  | ✓      | 56068.0    | 17.33        | 10.00         |
| server-base              | 7.1.32  | ✗      | 54208.0    | 17.96        | 9.67          |
| micro                    | 9.4.1   | ✗      | 53756.8    | 18.10        | 9.59          |
| fastify                  | 4.29.1  | ✓      | 52715.2    | 18.47        | 9.45          |
| yeps                     | 1.1.1   | ✗      | 52679.2    | 18.49        | 9.39          |
| connect-router           | 1.3.8   | ✓      | 50040.0    | 19.49        | 8.92          |
| micro-route              | 2.5.0   | ✓      | 48331.2    | 20.19        | 8.62          |
| trek-engine              | 1.0.5   | ✗      | 46997.6    | 20.78        | 7.71          |
| trek-router              | 1.2.0   | ✓      | 46238.4    | 21.13        | 7.58          |
| vapr                     | 0.6.0   | ✓      | 45256.8    | 21.60        | 7.42          |
| spirit                   | 0.6.1   | ✗      | 44295.2    | 22.12        | 7.90          |
| yeps-router              | 1.2.0   | ✓      | 43806.4    | 22.33        | 7.81          |
| spirit-router            | 0.5.0   | ✓      | 43444.0    | 22.50        | 7.75          |
| koa                      | 2.16.2  | ✗      | 40499.2    | 24.19        | 7.22          |
| total.js                 | 3.4.13  | ✓      | 39583.2    | 24.76        | 12.12         |
| restify                  | 8.6.1   | ✓      | 39198.6    | 25.02        | 7.06          |
| take-five                | 2.0.0   | ✓      | 39167.8    | 25.03        | 14.08         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37387.8    | 26.25        | 6.67          |
| koa-router               | 12.0.1  | ✓      | 34339.4    | 28.62        | 6.12          |
| hapi                     | 20.3.0  | ✓      | 32306.8    | 30.45        | 5.76          |
| microrouter              | 3.1.3   | ✓      | 30361.2    | 32.44        | 5.41          |
| trpc-router              | 9.27.4  | ✓      | 26477.6    | 37.26        | 5.86          |
| egg.js                   | 3.31.0  | ✓      | 17107.6    | 57.94        | 6.12          |
| express                  | 4.21.2  | ✓      | 13537.4    | 73.34        | 2.41          |
| express-with-middlewares | 4.21.2  | ✓      | 12583.4    | 78.91        | 4.68          |
| fastify-big-json         | 4.29.1  | ✓      | 12247.6    | 81.10        | 140.92        |
| express-route-prefix     | 4.21.2  | ✓      | 10974.4    | 90.54        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

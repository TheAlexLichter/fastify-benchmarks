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
* __Run:__ Mon Feb 26 2024 02:07:50 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| h3                       | 0.8.6   | ✗      | 67079.6    | 14.42        | 11.00         |
| polkadot                 | 1.0.0   | ✗      | 65950.8    | 14.65        | 11.76         |
| 0http                    | 3.5.2   | ✓      | 65024.0    | 14.88        | 11.60         |
| h3-router                | 0.8.6   | ✓      | 64937.6    | 14.90        | 10.65         |
| bare                     | 10.13.0 | ✗      | 59933.6    | 16.18        | 10.69         |
| foxify                   | 0.10.20 | ✓      | 58254.4    | 16.67        | 9.55          |
| polka                    | 0.5.2   | ✓      | 56600.0    | 17.17        | 10.09         |
| restana                  | 4.9.7   | ✓      | 56496.8    | 17.21        | 10.07         |
| micro                    | 9.4.1   | ✗      | 55871.2    | 17.40        | 9.96          |
| connect                  | 3.7.0   | ✗      | 55005.6    | 17.69        | 9.81          |
| fastify                  | 4.26.1  | ✓      | 54344.8    | 17.90        | 9.74          |
| server-base-router       | 7.1.32  | ✓      | 52936.0    | 18.39        | 9.44          |
| server-base              | 7.1.32  | ✗      | 52889.6    | 18.40        | 9.43          |
| yeps                     | 1.1.1   | ✗      | 52057.6    | 18.71        | 9.28          |
| micro-route              | 2.5.0   | ✓      | 49783.2    | 19.60        | 8.88          |
| connect-router           | 1.3.8   | ✓      | 49010.4    | 19.90        | 8.74          |
| trek-engine              | 1.0.5   | ✗      | 48183.2    | 20.26        | 7.90          |
| trek-router              | 1.2.0   | ✓      | 46783.2    | 20.87        | 7.67          |
| vapr                     | 0.6.0   | ✓      | 46058.4    | 21.21        | 7.55          |
| yeps-router              | 1.2.0   | ✓      | 44147.2    | 22.14        | 7.87          |
| spirit                   | 0.6.1   | ✗      | 43711.2    | 22.34        | 7.80          |
| koa                      | 2.15.0  | ✗      | 42084.0    | 23.25        | 7.51          |
| restify                  | 8.6.1   | ✓      | 39207.0    | 25.02        | 7.07          |
| take-five                | 2.0.0   | ✓      | 38893.0    | 25.22        | 13.98         |
| total.js                 | 3.4.13  | ✓      | 38840.0    | 25.23        | 11.89         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38812.2    | 25.26        | 6.92          |
| koa-router               | 12.0.1  | ✓      | 37043.0    | 26.49        | 6.61          |
| spirit-router            | 0.5.0   | ✓      | 34958.4    | 28.11        | 6.23          |
| hapi                     | 20.3.0  | ✓      | 33570.6    | 29.29        | 5.99          |
| microrouter              | 3.1.3   | ✓      | 32240.4    | 30.51        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 26692.0    | 36.95        | 5.91          |
| egg.js                   | 3.20.0  | ✓      | 17941.6    | 55.21        | 6.42          |
| express                  | 4.18.2  | ✓      | 13438.2    | 73.87        | 2.40          |
| fastify-big-json         | 4.26.1  | ✓      | 12872.8    | 77.14        | 148.11        |
| express-with-middlewares | 4.18.2  | ✓      | 12644.6    | 78.54        | 4.70          |
| express-route-prefix     | 4.18.2  | ✓      | 10985.4    | 90.47        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

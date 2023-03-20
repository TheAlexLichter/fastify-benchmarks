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
* __Run:__ Mon Mar 20 2023 02:35:36 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 56480.0    | 17.22        | 10.07         |
| foxify                   | 0.10.20 | ✓      | 55580.8    | 17.49        | 9.12          |
| micro                    | 9.4.1   | ✗      | 55553.6    | 17.50        | 9.91          |
| fastify                  | 4.14.1  | ✓      | 55242.4    | 17.60        | 9.90          |
| polka                    | 0.5.2   | ✓      | 55003.2    | 17.68        | 9.81          |
| polkadot                 | 1.0.0   | ✗      | 54644.8    | 17.81        | 9.75          |
| 0http                    | 3.5.1   | ✓      | 53776.0    | 18.11        | 9.59          |
| h3                       | 0.8.6   | ✗      | 53220.0    | 18.30        | 8.73          |
| h3-router                | 0.8.6   | ✓      | 51914.4    | 18.76        | 8.52          |
| yeps                     | 1.1.1   | ✗      | 51008.0    | 19.11        | 9.10          |
| connect                  | 3.7.0   | ✗      | 50893.6    | 19.16        | 9.08          |
| server-base-router       | 7.1.32  | ✓      | 50787.2    | 19.19        | 9.06          |
| server-base              | 7.1.32  | ✗      | 50666.4    | 19.24        | 9.04          |
| restana                  | 4.9.7   | ✓      | 49880.0    | 19.58        | 8.90          |
| connect-router           | 1.3.8   | ✓      | 48460.8    | 20.14        | 8.64          |
| micro-route              | 2.5.0   | ✓      | 47183.2    | 20.70        | 8.41          |
| trek-router              | 1.2.0   | ✓      | 44691.8    | 21.88        | 7.33          |
| trek-engine              | 1.0.5   | ✗      | 44470.4    | 22.00        | 7.29          |
| vapr                     | 0.6.0   | ✓      | 44092.0    | 22.18        | 7.23          |
| yeps-router              | 1.2.0   | ✓      | 41492.0    | 23.61        | 7.40          |
| koa                      | 2.14.1  | ✗      | 40787.0    | 24.02        | 7.27          |
| spirit                   | 0.6.1   | ✗      | 38647.2    | 25.38        | 6.89          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36991.4    | 26.53        | 6.60          |
| take-five                | 2.0.0   | ✓      | 36853.4    | 26.63        | 13.25         |
| total.js                 | 3.4.13  | ✓      | 36809.8    | 26.67        | 11.27         |
| spirit-router            | 0.5.0   | ✓      | 35961.8    | 27.32        | 6.41          |
| restify                  | 8.6.1   | ✓      | 35608.6    | 27.58        | 6.42          |
| koa-router               | 12.0.0  | ✓      | 33821.6    | 29.07        | 6.03          |
| hapi                     | 20.3.0  | ✓      | 29182.8    | 33.76        | 5.20          |
| microrouter              | 3.1.3   | ✓      | 28491.6    | 34.60        | 5.08          |
| trpc-router              | 9.27.3  | ✓      | 24732.8    | 39.94        | 5.47          |
| egg.js                   | 3.15.0  | ✓      | 14614.6    | 67.93        | 5.23          |
| express                  | 4.18.2  | ✓      | 11961.6    | 83.04        | 2.13          |
| express-with-middlewares | 4.18.2  | ✓      | 10480.3    | 94.86        | 3.90          |
| express-route-prefix     | 4.18.2  | ✓      | 10299.5    | 96.54        | 3.81          |
| fastify-big-json         | 4.14.1  | ✓      | 10167.5    | 97.97        | 116.99        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

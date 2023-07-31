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
* __Run:__ Mon Jul 31 2023 02:25:47 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 55513.6    | 17.52        | 9.90          |
| 0http                    | 3.5.2   | ✓      | 52653.6    | 18.50        | 9.39          |
| bare                     | 10.13.0 | ✗      | 52382.4    | 18.60        | 9.34          |
| polka                    | 0.5.2   | ✓      | 52186.4    | 18.66        | 9.31          |
| micro                    | 9.4.1   | ✗      | 51780.0    | 18.81        | 9.23          |
| foxify                   | 0.10.20 | ✓      | 51192.0    | 19.04        | 8.40          |
| fastify                  | 4.21.0  | ✓      | 51110.4    | 19.07        | 9.16          |
| h3-router                | 0.8.6   | ✓      | 51084.8    | 19.08        | 8.38          |
| connect                  | 3.7.0   | ✗      | 51039.2    | 19.10        | 9.10          |
| h3                       | 0.8.6   | ✗      | 50415.2    | 19.34        | 8.27          |
| server-base              | 7.1.32  | ✗      | 49740.8    | 19.61        | 8.87          |
| restana                  | 4.9.7   | ✓      | 49305.6    | 19.80        | 8.79          |
| server-base-router       | 7.1.32  | ✓      | 49235.2    | 19.81        | 8.78          |
| yeps                     | 1.1.1   | ✗      | 45760.0    | 21.35        | 8.16          |
| connect-router           | 1.3.8   | ✓      | 45207.2    | 21.62        | 8.06          |
| micro-route              | 2.5.0   | ✓      | 44539.2    | 21.95        | 7.94          |
| trek-engine              | 1.0.5   | ✗      | 44463.4    | 21.99        | 7.29          |
| trek-router              | 1.2.0   | ✓      | 42634.2    | 22.96        | 6.99          |
| vapr                     | 0.6.0   | ✓      | 40912.0    | 23.94        | 6.71          |
| yeps-router              | 1.2.0   | ✓      | 38677.4    | 25.37        | 6.90          |
| koa                      | 2.14.2  | ✗      | 38495.8    | 25.48        | 6.87          |
| spirit                   | 0.6.1   | ✗      | 38125.6    | 25.74        | 6.80          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36289.0    | 27.06        | 6.47          |
| take-five                | 2.0.0   | ✓      | 35769.0    | 27.48        | 12.86         |
| spirit-router            | 0.5.0   | ✓      | 35671.8    | 27.54        | 6.36          |
| restify                  | 8.6.1   | ✓      | 35519.4    | 27.65        | 6.40          |
| total.js                 | 3.4.13  | ✓      | 34565.0    | 28.43        | 10.58         |
| koa-router               | 12.0.0  | ✓      | 32386.6    | 30.38        | 5.78          |
| hapi                     | 20.3.0  | ✓      | 29145.6    | 33.81        | 5.20          |
| microrouter              | 3.1.3   | ✓      | 28182.4    | 34.98        | 5.03          |
| trpc-router              | 9.27.3  | ✓      | 23741.2    | 41.61        | 5.25          |
| egg.js                   | 3.17.3  | ✓      | 14500.2    | 68.45        | 5.19          |
| express                  | 4.18.2  | ✓      | 11983.4    | 82.89        | 2.14          |
| express-with-middlewares | 4.18.2  | ✓      | 10350.6    | 96.03        | 3.85          |
| express-route-prefix     | 4.18.2  | ✓      | 10093.3    | 98.54        | 3.73          |
| fastify-big-json         | 4.21.0  | ✓      | 9692.5     | 102.60       | 111.51        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

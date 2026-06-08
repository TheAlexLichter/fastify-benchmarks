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
* __Run:__ Mon Jun 08 2026 05:43:46 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68507.6    | 14.10        | 12.22         |
| 0http                    | 3.5.3   | ✓      | 66909.2    | 14.45        | 11.93         |
| h3-router                | 0.8.6   | ✓      | 64741.6    | 14.95        | 10.62         |
| h3                       | 0.8.6   | ✗      | 63213.2    | 15.32        | 10.37         |
| bare                     | 10.13.0 | ✗      | 59998.4    | 16.17        | 10.70         |
| foxify                   | 0.10.20 | ✓      | 59397.6    | 16.34        | 9.74          |
| restana                  | 4.9.9   | ✓      | 59210.4    | 16.39        | 10.56         |
| polka                    | 0.5.2   | ✓      | 58698.4    | 16.54        | 10.47         |
| micro                    | 9.4.1   | ✗      | 56835.2    | 17.10        | 10.14         |
| connect                  | 3.7.0   | ✗      | 56427.2    | 17.23        | 10.06         |
| fastify                  | 4.29.1  | ✓      | 55796.0    | 17.42        | 10.00         |
| server-base              | 7.1.32  | ✗      | 54837.6    | 17.74        | 9.78          |
| server-base-router       | 7.1.32  | ✓      | 54554.4    | 17.84        | 9.73          |
| yeps                     | 1.1.1   | ✗      | 53449.6    | 18.22        | 9.53          |
| connect-router           | 1.3.8   | ✓      | 50908.0    | 19.15        | 9.08          |
| trek-engine              | 1.0.5   | ✗      | 50248.8    | 19.40        | 8.24          |
| micro-route              | 2.5.0   | ✓      | 49387.2    | 19.75        | 8.81          |
| vapr                     | 0.6.0   | ✓      | 47766.4    | 20.44        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 47455.2    | 20.58        | 7.78          |
| spirit                   | 0.6.1   | ✗      | 44250.4    | 22.11        | 7.89          |
| yeps-router              | 1.2.0   | ✓      | 43408.8    | 22.54        | 7.74          |
| spirit-router            | 0.5.0   | ✓      | 43215.2    | 22.64        | 7.71          |
| koa                      | 2.16.4  | ✗      | 42536.0    | 23.01        | 7.59          |
| total.js                 | 3.4.13  | ✓      | 40647.2    | 24.09        | 12.44         |
| take-five                | 2.0.0   | ✓      | 39664.8    | 24.72        | 14.26         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38992.2    | 25.15        | 6.95          |
| restify                  | 8.6.1   | ✓      | 37910.6    | 25.88        | 6.83          |
| koa-router               | 12.0.1  | ✓      | 35178.2    | 27.92        | 6.27          |
| hapi                     | 20.3.0  | ✓      | 32699.2    | 30.08        | 5.83          |
| microrouter              | 3.1.3   | ✓      | 32021.2    | 30.73        | 5.71          |
| trpc-router              | 9.27.4  | ✓      | 27626.0    | 35.69        | 6.11          |
| egg.js                   | 3.34.0  | ✓      | 17567.9    | 56.42        | 6.28          |
| express                  | 4.22.2  | ✓      | 13060.4    | 76.03        | 2.33          |
| express-with-middlewares | 4.22.2  | ✓      | 12300.0    | 80.75        | 4.57          |
| fastify-big-json         | 4.29.1  | ✓      | 12250.8    | 81.08        | 140.96        |
| express-route-prefix     | 4.22.2  | ✓      | 10003.5    | 99.37        | 3.70          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

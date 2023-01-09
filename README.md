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
* __Node:__ `v14.21.1`
* __Run:__ Mon Jan 09 2023 02:32:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 62721.6    | 15.42        | 11.19         |
| bare                     | 10.13.0 | ✗      | 61996.8    | 15.63        | 11.06         |
| 0http                    | 3.4.2   | ✓      | 61424.0    | 15.77        | 10.95         |
| h3                       | 0.8.6   | ✗      | 60593.6    | 15.98        | 9.94          |
| h3-router                | 0.8.6   | ✓      | 60003.2    | 16.19        | 9.84          |
| foxify                   | 0.10.20 | ✓      | 59339.2    | 16.35        | 9.73          |
| polka                    | 0.5.2   | ✓      | 58728.0    | 16.53        | 10.47         |
| micro                    | 9.4.1   | ✗      | 58281.6    | 16.66        | 10.39         |
| server-base              | 7.1.32  | ✗      | 58031.2    | 16.74        | 10.35         |
| server-base-router       | 7.1.32  | ✓      | 57214.4    | 16.97        | 10.20         |
| connect                  | 3.7.0   | ✗      | 56543.2    | 17.20        | 10.08         |
| restana                  | 4.9.7   | ✓      | 56066.4    | 17.29        | 10.00         |
| yeps                     | 1.1.1   | ✗      | 55079.2    | 17.66        | 9.82          |
| connect-router           | 1.3.7   | ✓      | 53317.6    | 18.27        | 9.51          |
| micro-route              | 2.5.0   | ✓      | 52783.2    | 18.46        | 9.41          |
| trek-engine              | 1.0.5   | ✗      | 50481.6    | 19.31        | 8.28          |
| vapr                     | 0.6.0   | ✓      | 49959.2    | 19.52        | 8.19          |
| trek-router              | 1.2.0   | ✓      | 49169.6    | 19.84        | 8.07          |
| yeps-router              | 1.2.0   | ✓      | 46215.2    | 21.15        | 8.24          |
| koa                      | 2.14.1  | ✗      | 44842.4    | 21.80        | 8.00          |
| spirit                   | 0.6.1   | ✗      | 44816.8    | 21.81        | 7.99          |
| spirit-router            | 0.5.0   | ✓      | 44156.8    | 22.15        | 7.87          |
| fastify                  | 4.11.0  | ✓      | 43419.2    | 22.54        | 7.78          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41583.2    | 23.55        | 7.42          |
| take-five                | 2.0.0   | ✓      | 41534.4    | 23.56        | 14.93         |
| total.js                 | 3.4.13  | ✓      | 41412.8    | 23.65        | 12.68         |
| restify                  | 8.6.1   | ✓      | 39967.8    | 24.51        | 7.20          |
| koa-router               | 12.0.0  | ✓      | 38119.8    | 25.73        | 6.80          |
| hapi                     | 20.2.2  | ✓      | 34685.8    | 28.32        | 6.19          |
| microrouter              | 3.1.3   | ✓      | 33116.6    | 29.69        | 5.91          |
| trpc-router              | 9.27.3  | ✓      | 25280.8    | 39.04        | 5.59          |
| egg.js                   | 3.12.0  | ✓      | 16889.4    | 58.68        | 6.04          |
| express                  | 4.18.2  | ✓      | 14019.4    | 70.80        | 2.50          |
| express-with-middlewares | 4.18.2  | ✓      | 12405.0    | 80.05        | 4.61          |
| express-route-prefix     | 4.18.2  | ✓      | 12159.0    | 81.65        | 4.50          |
| fastify-big-json         | 4.11.0  | ✓      | 11696.4    | 84.98        | 134.58        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

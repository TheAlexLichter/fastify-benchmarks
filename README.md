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
* __Run:__ Mon Jun 22 2026 06:09:45 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 72567.6    | 13.29        | 12.94         |
| bare                     | 10.13.0 | ✗      | 70638.4    | 13.66        | 12.60         |
| 0http                    | 3.5.3   | ✓      | 69553.2    | 13.88        | 12.40         |
| foxify                   | 0.10.20 | ✓      | 69430.0    | 13.91        | 11.39         |
| polka                    | 0.5.2   | ✓      | 69426.0    | 13.91        | 12.38         |
| h3                       | 0.8.6   | ✗      | 68208.0    | 14.16        | 11.19         |
| connect                  | 3.7.0   | ✗      | 67957.2    | 14.22        | 12.12         |
| server-base-router       | 7.1.32  | ✓      | 67722.8    | 14.27        | 12.08         |
| h3-router                | 0.8.6   | ✓      | 66766.0    | 14.49        | 10.95         |
| fastify                  | 4.29.1  | ✓      | 65868.0    | 14.69        | 11.81         |
| restana                  | 4.9.9   | ✓      | 65784.0    | 14.69        | 11.73         |
| yeps                     | 1.1.1   | ✗      | 65493.2    | 14.76        | 11.68         |
| micro                    | 9.4.1   | ✗      | 65390.8    | 14.80        | 11.66         |
| server-base              | 7.1.32  | ✗      | 65140.4    | 14.85        | 11.62         |
| connect-router           | 1.3.8   | ✓      | 62934.4    | 15.39        | 11.22         |
| micro-route              | 2.5.0   | ✓      | 62530.0    | 15.50        | 11.15         |
| vapr                     | 0.6.0   | ✓      | 58839.2    | 16.50        | 9.65          |
| trek-engine              | 1.0.5   | ✗      | 54083.2    | 18.00        | 8.87          |
| trek-router              | 1.2.0   | ✓      | 53609.6    | 18.16        | 8.79          |
| yeps-router              | 1.2.0   | ✓      | 51093.6    | 19.07        | 9.11          |
| take-five                | 2.0.0   | ✓      | 49619.2    | 19.66        | 17.84         |
| total.js                 | 3.4.13  | ✓      | 49552.8    | 19.68        | 15.17         |
| koa                      | 2.16.4  | ✗      | 47733.6    | 20.45        | 8.51          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 46168.0    | 21.16        | 8.23          |
| restify                  | 8.6.1   | ✓      | 45503.2    | 21.48        | 8.20          |
| koa-router               | 12.0.1  | ✓      | 43250.4    | 22.62        | 7.71          |
| spirit                   | 0.6.1   | ✗      | 43124.0    | 22.68        | 7.69          |
| spirit-router            | 0.5.0   | ✓      | 40834.4    | 23.99        | 7.28          |
| microrouter              | 3.1.3   | ✓      | 40326.4    | 24.29        | 7.19          |
| hapi                     | 20.3.0  | ✓      | 37329.4    | 26.29        | 6.66          |
| trpc-router              | 9.27.4  | ✓      | 30624.2    | 32.15        | 6.78          |
| egg.js                   | 3.34.0  | ✓      | 18588.7    | 53.27        | 6.65          |
| express                  | 4.22.2  | ✓      | 16130.9    | 61.46        | 2.88          |
| express-with-middlewares | 4.22.2  | ✓      | 14992.4    | 66.17        | 5.58          |
| fastify-big-json         | 4.29.1  | ✓      | 12854.0    | 77.27        | 147.89        |
| express-route-prefix     | 4.22.2  | ✓      | 11884.0    | 83.60        | 4.40          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

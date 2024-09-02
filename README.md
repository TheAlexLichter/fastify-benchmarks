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
* __Run:__ Mon Sep 02 2024 02:33:33 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69615.6    | 13.86        | 12.41         |
| 0http                    | 3.5.3   | ✓      | 69416.8    | 13.91        | 12.38         |
| h3                       | 0.8.6   | ✗      | 64724.4    | 14.95        | 10.62         |
| h3-router                | 0.8.6   | ✓      | 64409.6    | 15.03        | 10.57         |
| restana                  | 4.9.9   | ✓      | 63135.2    | 15.34        | 11.26         |
| foxify                   | 0.10.20 | ✓      | 59948.8    | 16.18        | 9.83          |
| polka                    | 0.5.2   | ✓      | 58456.8    | 16.60        | 10.43         |
| bare                     | 10.13.0 | ✗      | 58350.4    | 16.65        | 10.41         |
| connect                  | 3.7.0   | ✗      | 57116.0    | 17.01        | 10.19         |
| micro                    | 9.4.1   | ✗      | 56393.6    | 17.23        | 10.06         |
| fastify                  | 4.28.1  | ✓      | 55074.4    | 17.66        | 9.87          |
| server-base              | 7.1.32  | ✗      | 52942.4    | 18.39        | 9.44          |
| server-base-router       | 7.1.32  | ✓      | 52371.2    | 18.60        | 9.34          |
| yeps                     | 1.1.1   | ✗      | 50963.2    | 19.13        | 9.09          |
| connect-router           | 1.3.8   | ✓      | 50483.2    | 19.31        | 9.00          |
| micro-route              | 2.5.0   | ✓      | 49861.6    | 19.56        | 8.89          |
| trek-router              | 1.2.0   | ✓      | 47688.8    | 20.47        | 7.82          |
| trek-engine              | 1.0.5   | ✗      | 47640.8    | 20.49        | 7.81          |
| vapr                     | 0.6.0   | ✓      | 46481.6    | 21.01        | 7.62          |
| yeps-router              | 1.2.0   | ✓      | 44132.8    | 22.16        | 7.87          |
| spirit-router            | 0.5.0   | ✓      | 43862.4    | 22.29        | 7.82          |
| koa                      | 2.15.3  | ✗      | 43366.4    | 22.56        | 7.73          |
| spirit                   | 0.6.1   | ✗      | 43036.8    | 22.76        | 7.68          |
| total.js                 | 3.4.13  | ✓      | 40356.0    | 24.28        | 12.35         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40248.8    | 24.34        | 7.18          |
| restify                  | 8.6.1   | ✓      | 39551.4    | 24.78        | 7.13          |
| take-five                | 2.0.0   | ✓      | 39153.8    | 25.04        | 14.08         |
| koa-router               | 12.0.1  | ✓      | 37647.4    | 26.06        | 6.71          |
| hapi                     | 20.3.0  | ✓      | 33312.6    | 29.52        | 5.94          |
| microrouter              | 3.1.3   | ✓      | 32206.0    | 30.54        | 5.74          |
| trpc-router              | 9.27.4  | ✓      | 26647.2    | 37.02        | 5.90          |
| egg.js                   | 3.27.1  | ✓      | 17550.3    | 56.47        | 6.28          |
| express                  | 4.19.2  | ✓      | 13528.8    | 73.37        | 2.41          |
| fastify-big-json         | 4.28.1  | ✓      | 12784.4    | 77.68        | 147.10        |
| express-with-middlewares | 4.19.2  | ✓      | 12410.4    | 80.01        | 4.62          |
| express-route-prefix     | 4.19.2  | ✓      | 10802.6    | 92.00        | 4.00          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

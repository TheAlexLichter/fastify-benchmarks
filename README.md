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
* __Run:__ Mon Oct 30 2023 02:07:54 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 62210.4    | 15.59        | 11.09         |
| bare                     | 10.13.0 | ✗      | 61765.6    | 15.70        | 11.01         |
| h3-router                | 0.8.6   | ✓      | 59493.6    | 16.33        | 9.76          |
| 0http                    | 3.5.2   | ✓      | 59268.0    | 16.38        | 10.57         |
| h3                       | 0.8.6   | ✗      | 59240.8    | 16.38        | 9.72          |
| foxify                   | 0.10.20 | ✓      | 57449.6    | 16.90        | 9.42          |
| polka                    | 0.5.2   | ✓      | 57335.2    | 16.94        | 10.22         |
| connect                  | 3.7.0   | ✗      | 57032.0    | 17.04        | 10.17         |
| fastify                  | 4.24.3  | ✓      | 56823.2    | 17.10        | 10.19         |
| micro                    | 9.4.1   | ✗      | 56500.8    | 17.19        | 10.08         |
| server-base-router       | 7.1.32  | ✓      | 55526.4    | 17.51        | 9.90          |
| server-base              | 7.1.32  | ✗      | 55072.8    | 17.66        | 9.82          |
| yeps                     | 1.1.1   | ✗      | 54458.4    | 17.86        | 9.71          |
| restana                  | 4.9.7   | ✓      | 54140.0    | 18.00        | 9.65          |
| connect-router           | 1.3.8   | ✓      | 52932.0    | 18.40        | 9.44          |
| micro-route              | 2.5.0   | ✓      | 52234.4    | 18.64        | 9.31          |
| trek-engine              | 1.0.5   | ✗      | 50292.0    | 19.38        | 8.25          |
| trek-router              | 1.2.0   | ✓      | 49317.6    | 19.78        | 8.09          |
| vapr                     | 0.6.0   | ✓      | 48635.2    | 20.06        | 7.98          |
| yeps-router              | 1.2.0   | ✓      | 44477.6    | 22.00        | 7.93          |
| spirit                   | 0.6.1   | ✗      | 44476.0    | 22.00        | 7.93          |
| koa                      | 2.14.2  | ✗      | 44172.8    | 22.14        | 7.88          |
| spirit-router            | 0.5.0   | ✓      | 43525.6    | 22.49        | 7.76          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 41566.4    | 23.55        | 7.41          |
| total.js                 | 3.4.13  | ✓      | 41159.2    | 23.80        | 12.60         |
| take-five                | 2.0.0   | ✓      | 40505.4    | 24.19        | 14.56         |
| restify                  | 8.6.1   | ✓      | 39585.6    | 24.77        | 7.13          |
| koa-router               | 12.0.1  | ✓      | 39021.4    | 25.12        | 6.96          |
| hapi                     | 20.3.0  | ✓      | 34286.2    | 28.67        | 6.11          |
| microrouter              | 3.1.3   | ✓      | 32531.6    | 30.23        | 5.80          |
| trpc-router              | 9.27.3  | ✓      | 27938.0    | 35.28        | 6.18          |
| egg.js                   | 3.17.5  | ✓      | 16384.0    | 60.53        | 5.86          |
| express                  | 4.18.2  | ✓      | 13636.6    | 72.79        | 2.43          |
| fastify-big-json         | 4.24.3  | ✓      | 12022.0    | 82.69        | 138.32        |
| express-with-middlewares | 4.18.2  | ✓      | 11861.0    | 83.76        | 4.41          |
| express-route-prefix     | 4.18.2  | ✓      | 10098.0    | 98.46        | 3.74          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

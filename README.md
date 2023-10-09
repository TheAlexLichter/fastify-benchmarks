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
* __Run:__ Mon Oct 09 2023 02:07:26 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 56127.2    | 17.32        | 10.01         |
| foxify                   | 0.10.20 | ✓      | 54476.0    | 17.86        | 8.93          |
| bare                     | 10.13.0 | ✗      | 54456.8    | 17.87        | 9.71          |
| micro                    | 9.4.1   | ✗      | 54239.2    | 17.94        | 9.67          |
| polka                    | 0.5.2   | ✓      | 54104.0    | 17.98        | 9.65          |
| fastify                  | 4.23.2  | ✓      | 53460.0    | 18.22        | 9.58          |
| 0http                    | 3.5.2   | ✓      | 53029.6    | 18.39        | 9.46          |
| h3-router                | 0.8.6   | ✓      | 52985.6    | 18.37        | 8.69          |
| connect                  | 3.7.0   | ✗      | 52775.2    | 18.45        | 9.41          |
| h3                       | 0.8.6   | ✗      | 52639.2    | 18.51        | 8.63          |
| server-base-router       | 7.1.32  | ✓      | 51684.8    | 18.85        | 9.22          |
| server-base              | 7.1.32  | ✗      | 51017.6    | 19.10        | 9.10          |
| yeps                     | 1.1.1   | ✗      | 50650.4    | 19.25        | 9.03          |
| restana                  | 4.9.7   | ✓      | 49199.2    | 19.82        | 8.77          |
| connect-router           | 1.3.8   | ✓      | 48956.8    | 19.93        | 8.73          |
| micro-route              | 2.5.0   | ✓      | 47596.8    | 20.51        | 8.49          |
| trek-engine              | 1.0.5   | ✗      | 45355.2    | 21.55        | 7.44          |
| trek-router              | 1.2.0   | ✓      | 45039.8    | 21.70        | 7.39          |
| vapr                     | 0.6.0   | ✓      | 43425.4    | 22.54        | 7.12          |
| yeps-router              | 1.2.0   | ✓      | 41064.8    | 23.86        | 7.32          |
| koa                      | 2.14.2  | ✗      | 40537.4    | 24.18        | 7.23          |
| spirit                   | 0.6.1   | ✗      | 39277.6    | 24.98        | 7.00          |
| spirit-router            | 0.5.0   | ✓      | 37668.8    | 26.06        | 6.72          |
| take-five                | 2.0.0   | ✓      | 37503.0    | 26.17        | 13.48         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 37391.0    | 26.26        | 6.67          |
| total.js                 | 3.4.13  | ✓      | 37207.0    | 26.38        | 11.39         |
| restify                  | 8.6.1   | ✓      | 37069.0    | 26.48        | 6.68          |
| koa-router               | 12.0.0  | ✓      | 34191.4    | 28.76        | 6.10          |
| hapi                     | 20.3.0  | ✓      | 29628.8    | 33.25        | 5.28          |
| microrouter              | 3.1.3   | ✓      | 29314.0    | 33.62        | 5.23          |
| trpc-router              | 9.27.3  | ✓      | 24721.2    | 39.94        | 5.47          |
| egg.js                   | 3.17.4  | ✓      | 14493.0    | 68.48        | 5.18          |
| express                  | 4.18.2  | ✓      | 11606.6    | 85.59        | 2.07          |
| express-with-middlewares | 4.18.2  | ✓      | 10259.9    | 96.93        | 3.82          |
| fastify-big-json         | 4.23.2  | ✓      | 9818.5     | 101.40       | 112.97        |
| express-route-prefix     | 4.18.2  | ✓      | 8853.0     | 112.37       | 3.28          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

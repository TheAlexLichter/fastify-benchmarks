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
* __Run:__ Mon Jul 15 2024 02:27:25 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68986.4    | 13.99        | 12.30         |
| 0http                    | 3.5.3   | ✓      | 65246.0    | 14.85        | 11.64         |
| h3                       | 0.8.6   | ✗      | 65210.0    | 14.84        | 10.70         |
| h3-router                | 0.8.6   | ✓      | 61048.8    | 15.89        | 10.01         |
| foxify                   | 0.10.20 | ✓      | 60048.8    | 16.15        | 9.85          |
| bare                     | 10.13.0 | ✗      | 59308.0    | 16.36        | 10.58         |
| polka                    | 0.5.2   | ✓      | 58440.8    | 16.61        | 10.42         |
| restana                  | 4.9.9   | ✓      | 58055.2    | 16.72        | 10.35         |
| connect                  | 3.7.0   | ✗      | 57566.4    | 16.88        | 10.27         |
| micro                    | 9.4.1   | ✗      | 55788.0    | 17.43        | 9.95          |
| fastify                  | 4.28.1  | ✓      | 54690.4    | 17.79        | 9.80          |
| server-base              | 7.1.32  | ✗      | 54080.8    | 17.99        | 9.64          |
| server-base-router       | 7.1.32  | ✓      | 53647.2    | 18.14        | 9.57          |
| yeps                     | 1.1.1   | ✗      | 52881.6    | 18.41        | 9.43          |
| micro-route              | 2.5.0   | ✓      | 49547.2    | 19.68        | 8.84          |
| connect-router           | 1.3.8   | ✓      | 48929.6    | 19.94        | 8.73          |
| trek-engine              | 1.0.5   | ✗      | 47797.6    | 20.43        | 7.84          |
| trek-router              | 1.2.0   | ✓      | 47732.8    | 20.46        | 7.83          |
| vapr                     | 0.6.0   | ✓      | 45428.0    | 21.51        | 7.45          |
| spirit                   | 0.6.1   | ✗      | 44580.0    | 21.95        | 7.95          |
| yeps-router              | 1.2.0   | ✓      | 44284.0    | 22.09        | 7.90          |
| spirit-router            | 0.5.0   | ✓      | 43264.8    | 22.57        | 7.72          |
| koa                      | 2.15.3  | ✗      | 42725.6    | 22.91        | 7.62          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39532.8    | 24.80        | 7.05          |
| restify                  | 8.6.1   | ✓      | 38942.4    | 25.18        | 7.02          |
| total.js                 | 3.4.13  | ✓      | 38668.0    | 25.36        | 11.84         |
| take-five                | 2.0.0   | ✓      | 38381.0    | 25.55        | 13.80         |
| koa-router               | 12.0.1  | ✓      | 37336.6    | 26.27        | 6.66          |
| hapi                     | 20.3.0  | ✓      | 33430.4    | 29.41        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 31613.2    | 31.13        | 5.64          |
| trpc-router              | 9.27.4  | ✓      | 26635.6    | 37.03        | 5.89          |
| egg.js                   | 3.27.1  | ✓      | 17411.4    | 56.92        | 6.23          |
| express                  | 4.19.2  | ✓      | 13739.2    | 72.23        | 2.45          |
| fastify-big-json         | 4.28.1  | ✓      | 13005.8    | 76.35        | 149.64        |
| express-with-middlewares | 4.19.2  | ✓      | 12342.0    | 80.45        | 4.59          |
| express-route-prefix     | 4.19.2  | ✓      | 10904.8    | 91.12        | 4.04          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

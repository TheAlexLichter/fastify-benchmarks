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
* __Run:__ Mon Mar 16 2026 04:15:50 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66840.0    | 14.46        | 11.92         |
| polkadot                 | 1.0.0   | ✗      | 64365.6    | 15.03        | 11.48         |
| h3                       | 0.8.6   | ✗      | 63093.2    | 15.35        | 10.35         |
| h3-router                | 0.8.6   | ✓      | 61921.6    | 15.65        | 10.16         |
| restana                  | 4.9.9   | ✓      | 57741.6    | 16.82        | 10.30         |
| bare                     | 10.13.0 | ✗      | 57530.4    | 16.88        | 10.26         |
| micro                    | 9.4.1   | ✗      | 57105.6    | 17.01        | 10.18         |
| polka                    | 0.5.2   | ✓      | 57093.6    | 17.02        | 10.18         |
| foxify                   | 0.10.20 | ✓      | 56973.6    | 17.05        | 9.34          |
| connect                  | 3.7.0   | ✗      | 56210.4    | 17.30        | 10.02         |
| server-base              | 7.1.32  | ✗      | 56047.2    | 17.35        | 9.99          |
| fastify                  | 4.29.1  | ✓      | 54564.0    | 17.83        | 9.78          |
| server-base-router       | 7.1.32  | ✓      | 52909.6    | 18.40        | 9.44          |
| yeps                     | 1.1.1   | ✗      | 51806.4    | 18.80        | 9.24          |
| micro-route              | 2.5.0   | ✓      | 50013.6    | 19.50        | 8.92          |
| connect-router           | 1.3.8   | ✓      | 49848.0    | 19.56        | 8.89          |
| trek-engine              | 1.0.5   | ✗      | 47507.2    | 20.55        | 7.79          |
| trek-router              | 1.2.0   | ✓      | 46522.4    | 21.00        | 7.63          |
| vapr                     | 0.6.0   | ✓      | 44481.6    | 21.98        | 7.30          |
| spirit                   | 0.6.1   | ✗      | 43125.6    | 22.70        | 7.69          |
| yeps-router              | 1.2.0   | ✓      | 42031.2    | 23.29        | 7.50          |
| koa                      | 2.16.4  | ✗      | 41880.0    | 23.37        | 7.47          |
| spirit-router            | 0.5.0   | ✓      | 39982.4    | 24.52        | 7.13          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39778.6    | 24.64        | 7.09          |
| total.js                 | 3.4.13  | ✓      | 39684.0    | 24.70        | 12.15         |
| restify                  | 8.6.1   | ✓      | 37290.2    | 26.32        | 6.72          |
| take-five                | 2.0.0   | ✓      | 37067.0    | 26.48        | 13.33         |
| koa-router               | 12.0.1  | ✓      | 35729.8    | 27.49        | 6.37          |
| hapi                     | 20.3.0  | ✓      | 32514.0    | 30.25        | 5.80          |
| microrouter              | 3.1.3   | ✓      | 31079.6    | 31.67        | 5.54          |
| trpc-router              | 9.27.4  | ✓      | 26581.6    | 37.11        | 5.88          |
| egg.js                   | 3.34.0  | ✓      | 17041.0    | 58.17        | 6.09          |
| express                  | 4.22.1  | ✓      | 13168.2    | 75.38        | 2.35          |
| express-with-middlewares | 4.22.1  | ✓      | 12237.2    | 81.14        | 4.55          |
| fastify-big-json         | 4.29.1  | ✓      | 12233.2    | 81.20        | 140.76        |
| express-route-prefix     | 4.22.1  | ✓      | 10683.4    | 93.00        | 3.95          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

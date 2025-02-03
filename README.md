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
* __Run:__ Mon Feb 03 2025 02:37:02 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 68967.6    | 14.00        | 12.30         |
| 0http                    | 3.5.3   | ✓      | 68601.2    | 14.09        | 12.23         |
| h3                       | 0.8.6   | ✗      | 66610.4    | 14.52        | 10.93         |
| h3-router                | 0.8.6   | ✓      | 60568.0    | 16.02        | 9.94          |
| restana                  | 4.9.9   | ✓      | 59981.6    | 16.17        | 10.70         |
| foxify                   | 0.10.20 | ✓      | 59704.0    | 16.26        | 9.79          |
| bare                     | 10.13.0 | ✗      | 58661.6    | 16.55        | 10.46         |
| connect                  | 3.7.0   | ✗      | 57872.8    | 16.78        | 10.32         |
| polka                    | 0.5.2   | ✓      | 56760.0    | 17.12        | 10.12         |
| fastify                  | 4.29.0  | ✓      | 55720.0    | 17.45        | 9.99          |
| micro                    | 9.4.1   | ✗      | 55706.4    | 17.45        | 9.93          |
| server-base              | 7.1.32  | ✗      | 53648.0    | 18.14        | 9.57          |
| server-base-router       | 7.1.32  | ✓      | 52158.4    | 18.68        | 9.30          |
| yeps                     | 1.1.1   | ✗      | 51630.4    | 18.88        | 9.21          |
| connect-router           | 1.3.8   | ✓      | 50259.2    | 19.41        | 8.96          |
| micro-route              | 2.5.0   | ✓      | 49643.2    | 19.64        | 8.85          |
| trek-engine              | 1.0.5   | ✗      | 47712.0    | 20.46        | 7.83          |
| trek-router              | 1.2.0   | ✓      | 46952.0    | 20.81        | 7.70          |
| vapr                     | 0.6.0   | ✓      | 45964.0    | 21.25        | 7.54          |
| spirit                   | 0.6.1   | ✗      | 43242.4    | 22.62        | 7.71          |
| yeps-router              | 1.2.0   | ✓      | 43179.2    | 22.66        | 7.70          |
| koa                      | 2.15.3  | ✗      | 42196.8    | 23.20        | 7.53          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39513.6    | 24.81        | 7.05          |
| restify                  | 8.6.1   | ✓      | 38647.8    | 25.37        | 6.97          |
| total.js                 | 3.4.13  | ✓      | 38441.6    | 25.51        | 11.77         |
| take-five                | 2.0.0   | ✓      | 38321.0    | 25.60        | 13.78         |
| koa-router               | 12.0.1  | ✓      | 37206.2    | 26.38        | 6.64          |
| spirit-router            | 0.5.0   | ✓      | 34231.0    | 28.72        | 6.10          |
| hapi                     | 20.3.0  | ✓      | 33993.4    | 28.90        | 6.06          |
| microrouter              | 3.1.3   | ✓      | 32191.4    | 30.57        | 5.74          |
| trpc-router              | 9.27.4  | ✓      | 27406.8    | 35.98        | 6.06          |
| egg.js                   | 3.30.1  | ✓      | 17611.2    | 56.26        | 6.30          |
| express                  | 4.21.2  | ✓      | 13613.4    | 72.92        | 2.43          |
| fastify-big-json         | 4.29.0  | ✓      | 12849.0    | 77.28        | 147.83        |
| express-with-middlewares | 4.21.2  | ✓      | 12242.4    | 81.12        | 4.55          |
| express-route-prefix     | 4.21.2  | ✓      | 11166.0    | 88.97        | 4.13          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

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
* __Run:__ Mon Aug 07 2023 02:24:08 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 31474.8    | 31.28        | 5.61          |
| bare                     | 10.13.0 | ✗      | 31032.8    | 31.74        | 5.53          |
| micro                    | 9.4.1   | ✗      | 29475.2    | 33.43        | 5.26          |
| 0http                    | 3.5.2   | ✓      | 28703.6    | 34.36        | 5.12          |
| h3                       | 0.8.6   | ✗      | 28086.4    | 35.11        | 4.61          |
| fastify                  | 4.21.0  | ✓      | 27851.2    | 35.41        | 4.99          |
| foxify                   | 0.10.20 | ✓      | 27843.2    | 35.42        | 4.57          |
| h3-router                | 0.8.6   | ✓      | 27695.2    | 35.61        | 4.54          |
| connect                  | 3.7.0   | ✗      | 27325.7    | 36.14        | 4.87          |
| server-base-router       | 7.1.32  | ✓      | 25841.2    | 38.20        | 4.61          |
| server-base              | 7.1.32  | ✗      | 25752.0    | 38.33        | 4.59          |
| yeps                     | 1.1.1   | ✗      | 25610.0    | 38.56        | 4.57          |
| trek-engine              | 1.0.5   | ✗      | 25128.3    | 39.29        | 4.12          |
| polka                    | 0.5.2   | ✓      | 25020.4    | 39.46        | 4.46          |
| micro-route              | 2.5.0   | ✓      | 24774.0    | 39.86        | 4.42          |
| connect-router           | 1.3.8   | ✓      | 24380.0    | 40.51        | 4.35          |
| spirit                   | 0.6.1   | ✗      | 24213.6    | 40.81        | 4.32          |
| restana                  | 4.9.7   | ✓      | 23803.6    | 41.52        | 4.24          |
| trek-router              | 1.2.0   | ✓      | 23490.1    | 42.08        | 3.85          |
| yeps-router              | 1.2.0   | ✓      | 22923.6    | 43.12        | 4.09          |
| vapr                     | 0.6.0   | ✓      | 22880.8    | 43.19        | 3.75          |
| spirit-router            | 0.5.0   | ✓      | 22701.6    | 43.57        | 4.05          |
| koa                      | 2.14.2  | ✗      | 20976.0    | 47.17        | 3.74          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20576.8    | 48.11        | 3.67          |
| take-five                | 2.0.0   | ✓      | 20164.7    | 49.09        | 7.25          |
| restify                  | 8.6.1   | ✓      | 20052.9    | 49.35        | 3.61          |
| total.js                 | 3.4.13  | ✓      | 19728.7    | 50.19        | 6.04          |
| koa-router               | 12.0.0  | ✓      | 18945.7    | 52.26        | 3.38          |
| hapi                     | 20.3.0  | ✓      | 18276.9    | 54.21        | 3.26          |
| microrouter              | 3.1.3   | ✓      | 17384.0    | 57.04        | 3.10          |
| trpc-router              | 9.27.3  | ✓      | 16475.9    | 60.19        | 3.65          |
| egg.js                   | 3.17.4  | ✓      | 8664.3     | 115.00       | 3.10          |
| express                  | 4.18.2  | ✓      | 7186.3     | 138.47       | 1.28          |
| fastify-big-json         | 4.21.0  | ✓      | 6625.2     | 150.55       | 76.23         |
| express-route-prefix     | 4.18.2  | ✓      | 6568.2     | 151.58       | 2.43          |
| express-with-middlewares | 4.18.2  | ✓      | 6348.6     | 156.72       | 2.36          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

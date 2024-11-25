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
* __Run:__ Mon Nov 25 2024 02:45:45 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 65403.2    | 14.80        | 11.66         |
| polkadot                 | 1.0.0   | ✗      | 64066.8    | 15.11        | 11.43         |
| h3                       | 0.8.6   | ✗      | 58868.8    | 16.49        | 9.66          |
| restana                  | 4.9.9   | ✓      | 58308.0    | 16.64        | 10.40         |
| bare                     | 10.13.0 | ✗      | 57899.2    | 16.77        | 10.33         |
| foxify                   | 0.10.20 | ✓      | 57767.2    | 16.80        | 9.48          |
| h3-router                | 0.8.6   | ✓      | 57741.6    | 16.82        | 9.47          |
| polka                    | 0.5.2   | ✓      | 56931.2    | 17.07        | 10.15         |
| fastify                  | 4.28.1  | ✓      | 55800.0    | 17.43        | 10.00         |
| connect                  | 3.7.0   | ✗      | 55077.6    | 17.67        | 9.82          |
| micro                    | 9.4.1   | ✗      | 54458.4    | 17.86        | 9.71          |
| server-base-router       | 7.1.32  | ✓      | 53612.0    | 18.16        | 9.56          |
| yeps                     | 1.1.1   | ✗      | 52244.0    | 18.65        | 9.32          |
| server-base              | 7.1.32  | ✗      | 51135.2    | 19.06        | 9.12          |
| connect-router           | 1.3.8   | ✓      | 49772.0    | 19.60        | 8.88          |
| micro-route              | 2.5.0   | ✓      | 48013.6    | 20.33        | 8.56          |
| trek-engine              | 1.0.5   | ✗      | 47452.0    | 20.58        | 7.78          |
| trek-router              | 1.2.0   | ✓      | 47029.6    | 20.76        | 7.71          |
| vapr                     | 0.6.0   | ✓      | 44856.8    | 21.80        | 7.36          |
| yeps-router              | 1.2.0   | ✓      | 42552.8    | 22.99        | 7.59          |
| koa                      | 2.15.3  | ✗      | 41333.6    | 23.68        | 7.37          |
| spirit                   | 0.6.1   | ✗      | 39962.4    | 24.53        | 7.13          |
| spirit-router            | 0.5.0   | ✓      | 39705.6    | 24.69        | 7.08          |
| total.js                 | 3.4.13  | ✓      | 39122.6    | 25.06        | 11.98         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38742.6    | 25.31        | 6.91          |
| take-five                | 2.0.0   | ✓      | 38185.0    | 25.68        | 13.73         |
| restify                  | 8.6.1   | ✓      | 37565.0    | 26.12        | 6.77          |
| koa-router               | 12.0.1  | ✓      | 36119.4    | 27.18        | 6.44          |
| hapi                     | 20.3.0  | ✓      | 32107.6    | 30.64        | 5.73          |
| microrouter              | 3.1.3   | ✓      | 31061.2    | 31.68        | 5.54          |
| trpc-router              | 9.27.4  | ✓      | 26544.8    | 37.16        | 5.87          |
| egg.js                   | 3.28.0  | ✓      | 17304.3    | 57.26        | 6.19          |
| express                  | 4.21.1  | ✓      | 13529.6    | 73.35        | 2.41          |
| fastify-big-json         | 4.28.1  | ✓      | 12582.6    | 78.93        | 144.78        |
| express-with-middlewares | 4.21.1  | ✓      | 12503.4    | 79.42        | 4.65          |
| express-route-prefix     | 4.21.1  | ✓      | 10822.8    | 91.81        | 4.00          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

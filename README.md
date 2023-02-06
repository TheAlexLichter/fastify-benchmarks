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
* __Node:__ `v14.21.2`
* __Run:__ Mon Feb 06 2023 02:32:53 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 51707.2    | 18.90        | 9.22          |
| 0http                    | 3.4.2   | ✓      | 51260.0    | 19.07        | 9.14          |
| micro                    | 9.4.1   | ✗      | 51240.8    | 19.06        | 9.14          |
| polka                    | 0.5.2   | ✓      | 50703.2    | 19.28        | 9.04          |
| bare                     | 10.13.0 | ✗      | 50656.0    | 19.28        | 9.03          |
| fastify                  | 4.12.0  | ✓      | 50393.6    | 19.40        | 9.03          |
| foxify                   | 0.10.20 | ✓      | 50159.2    | 19.49        | 8.23          |
| connect                  | 3.7.0   | ✗      | 50099.2    | 19.49        | 8.93          |
| h3                       | 0.8.6   | ✗      | 49396.8    | 19.82        | 8.10          |
| server-base-router       | 7.1.32  | ✓      | 49179.2    | 19.87        | 8.77          |
| h3-router                | 0.8.6   | ✓      | 48800.8    | 20.06        | 8.00          |
| server-base              | 7.1.32  | ✗      | 48172.0    | 20.28        | 8.59          |
| yeps                     | 1.1.1   | ✗      | 47745.6    | 20.49        | 8.51          |
| restana                  | 4.9.7   | ✓      | 47742.4    | 20.50        | 8.51          |
| connect-router           | 1.3.7   | ✓      | 46423.2    | 21.08        | 8.28          |
| trek-engine              | 1.0.5   | ✗      | 44938.2    | 21.79        | 7.37          |
| micro-route              | 2.5.0   | ✓      | 44888.2    | 21.83        | 8.00          |
| trek-router              | 1.2.0   | ✓      | 43239.4    | 22.68        | 7.09          |
| vapr                     | 0.6.0   | ✓      | 41596.6    | 23.57        | 6.82          |
| yeps-router              | 1.2.0   | ✓      | 40768.8    | 24.06        | 7.27          |
| spirit                   | 0.6.1   | ✗      | 40295.2    | 24.38        | 7.19          |
| koa                      | 2.14.1  | ✗      | 39839.0    | 24.62        | 7.10          |
| spirit-router            | 0.5.0   | ✓      | 39125.4    | 25.12        | 6.98          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 36794.6    | 26.74        | 6.56          |
| restify                  | 8.6.1   | ✓      | 36741.0    | 26.75        | 6.62          |
| total.js                 | 3.4.13  | ✓      | 36369.0    | 27.05        | 11.13         |
| take-five                | 2.0.0   | ✓      | 36095.6    | 27.27        | 12.98         |
| koa-router               | 12.0.0  | ✓      | 33377.6    | 29.53        | 5.95          |
| hapi                     | 20.2.2  | ✓      | 29310.8    | 33.64        | 5.23          |
| microrouter              | 3.1.3   | ✓      | 28218.0    | 34.99        | 5.03          |
| trpc-router              | 9.27.3  | ✓      | 24750.4    | 39.92        | 5.48          |
| egg.js                   | 3.15.0  | ✓      | 14807.4    | 67.14        | 5.30          |
| express                  | 4.18.2  | ✓      | 12097.2    | 82.13        | 2.16          |
| express-with-middlewares | 4.18.2  | ✓      | 10373.6    | 95.84        | 3.86          |
| express-route-prefix     | 4.18.2  | ✓      | 9998.3     | 99.44        | 3.70          |
| fastify-big-json         | 4.12.0  | ✓      | 9835.8     | 101.24       | 113.16        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

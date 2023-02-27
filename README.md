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
* __Run:__ Mon Feb 27 2023 02:40:36 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 57199.2    | 16.99        | 10.20         |
| foxify                   | 0.10.20 | ✓      | 56572.8    | 17.18        | 9.28          |
| polka                    | 0.5.2   | ✓      | 56450.4    | 17.22        | 10.07         |
| h3                       | 0.8.6   | ✗      | 55591.2    | 17.49        | 9.12          |
| polkadot                 | 1.0.0   | ✗      | 55481.6    | 17.53        | 9.89          |
| micro                    | 9.4.1   | ✗      | 55369.6    | 17.57        | 9.87          |
| 0http                    | 3.4.4   | ✓      | 55278.4    | 17.60        | 9.86          |
| fastify                  | 4.13.0  | ✓      | 54981.6    | 17.69        | 9.86          |
| connect                  | 3.7.0   | ✗      | 54756.6    | 17.78        | 9.77          |
| server-base-router       | 7.1.32  | ✓      | 54052.8    | 18.00        | 9.64          |
| server-base              | 7.1.32  | ✗      | 53518.4    | 18.19        | 9.54          |
| h3-router                | 0.8.6   | ✓      | 53334.4    | 18.26        | 8.75          |
| yeps                     | 1.1.1   | ✗      | 51538.4    | 18.91        | 9.19          |
| restana                  | 4.9.7   | ✓      | 50525.6    | 19.26        | 9.01          |
| connect-router           | 1.3.8   | ✓      | 49364.8    | 19.76        | 8.80          |
| micro-route              | 2.5.0   | ✓      | 49185.6    | 19.83        | 8.77          |
| trek-engine              | 1.0.5   | ✗      | 46700.8    | 20.92        | 7.66          |
| trek-router              | 1.2.0   | ✓      | 45901.8    | 21.28        | 7.53          |
| vapr                     | 0.6.0   | ✓      | 44033.6    | 22.21        | 7.22          |
| yeps-router              | 1.2.0   | ✓      | 41204.0    | 23.77        | 7.35          |
| koa                      | 2.14.1  | ✗      | 40762.2    | 24.04        | 7.27          |
| spirit                   | 0.6.1   | ✗      | 40417.6    | 24.25        | 7.21          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38418.2    | 25.54        | 6.85          |
| total.js                 | 3.4.13  | ✓      | 37966.2    | 25.84        | 11.62         |
| spirit-router            | 0.5.0   | ✓      | 37725.0    | 26.03        | 6.73          |
| take-five                | 2.0.0   | ✓      | 36938.6    | 26.57        | 13.28         |
| restify                  | 8.6.1   | ✓      | 36831.8    | 26.64        | 6.64          |
| koa-router               | 12.0.0  | ✓      | 34542.6    | 28.45        | 6.16          |
| hapi                     | 20.3.0  | ✓      | 30524.0    | 32.26        | 5.44          |
| microrouter              | 3.1.3   | ✓      | 28991.2    | 33.98        | 5.17          |
| trpc-router              | 9.27.3  | ✓      | 25580.8    | 38.59        | 5.66          |
| egg.js                   | 3.15.0  | ✓      | 14803.6    | 67.04        | 5.29          |
| express                  | 4.18.2  | ✓      | 12202.4    | 81.42        | 2.18          |
| express-route-prefix     | 4.18.2  | ✓      | 10817.6    | 91.89        | 4.00          |
| fastify-big-json         | 4.13.0  | ✓      | 10633.0    | 93.56        | 122.34        |
| express-with-middlewares | 4.18.2  | ✓      | 10561.5    | 94.13        | 3.93          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

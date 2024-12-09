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
* __Run:__ Mon Dec 09 2024 02:51:21 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 69722.0    | 13.84        | 12.43         |
| polkadot                 | 1.0.0   | ✗      | 67200.4    | 14.39        | 11.98         |
| h3                       | 0.8.6   | ✗      | 66320.0    | 14.58        | 10.88         |
| bare                     | 10.13.0 | ✗      | 59676.0    | 16.26        | 10.64         |
| foxify                   | 0.10.20 | ✓      | 59376.8    | 16.34        | 9.74          |
| h3-router                | 0.8.6   | ✓      | 59202.4    | 16.40        | 9.71          |
| restana                  | 4.9.9   | ✓      | 58768.8    | 16.49        | 10.48         |
| connect                  | 3.7.0   | ✗      | 57323.2    | 16.95        | 10.22         |
| polka                    | 0.5.2   | ✓      | 57142.4    | 17.00        | 10.19         |
| micro                    | 9.4.1   | ✗      | 56802.4    | 17.11        | 10.13         |
| fastify                  | 4.29.0  | ✓      | 54636.0    | 17.80        | 9.79          |
| server-base-router       | 7.1.32  | ✓      | 53406.4    | 18.23        | 9.52          |
| server-base              | 7.1.32  | ✗      | 52826.4    | 18.43        | 9.42          |
| yeps                     | 1.1.1   | ✗      | 52373.6    | 18.59        | 9.34          |
| micro-route              | 2.5.0   | ✓      | 49867.2    | 19.56        | 8.89          |
| connect-router           | 1.3.8   | ✓      | 49788.0    | 19.59        | 8.88          |
| trek-router              | 1.2.0   | ✓      | 48241.6    | 20.24        | 7.91          |
| trek-engine              | 1.0.5   | ✗      | 48142.4    | 20.28        | 7.90          |
| vapr                     | 0.6.0   | ✓      | 45166.4    | 21.63        | 7.41          |
| spirit                   | 0.6.1   | ✗      | 44703.2    | 21.91        | 7.97          |
| yeps-router              | 1.2.0   | ✓      | 44600.0    | 21.94        | 7.95          |
| koa                      | 2.15.3  | ✗      | 43476.0    | 22.50        | 7.75          |
| spirit-router            | 0.5.0   | ✓      | 43172.8    | 22.65        | 7.70          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40011.4    | 24.49        | 7.14          |
| total.js                 | 3.4.13  | ✓      | 39284.0    | 24.96        | 12.02         |
| restify                  | 8.6.1   | ✓      | 38980.2    | 25.16        | 7.03          |
| take-five                | 2.0.0   | ✓      | 37783.8    | 25.96        | 13.59         |
| koa-router               | 12.0.1  | ✓      | 37670.6    | 26.05        | 6.72          |
| hapi                     | 20.3.0  | ✓      | 33780.2    | 29.10        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 31649.6    | 31.09        | 5.64          |
| trpc-router              | 9.27.4  | ✓      | 26381.6    | 37.39        | 5.84          |
| egg.js                   | 3.29.0  | ✓      | 17628.3    | 56.21        | 6.30          |
| express                  | 4.21.2  | ✓      | 13656.0    | 72.69        | 2.44          |
| fastify-big-json         | 4.29.0  | ✓      | 13105.0    | 75.77        | 150.78        |
| express-with-middlewares | 4.21.2  | ✓      | 12346.4    | 80.45        | 4.59          |
| express-route-prefix     | 4.21.2  | ✓      | 11011.2    | 90.24        | 4.07          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

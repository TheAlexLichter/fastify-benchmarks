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
* __Run:__ Mon Nov 27 2023 02:11:29 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 67662.0    | 14.30        | 12.07         |
| 0http                    | 3.5.2   | ✓      | 63842.8    | 15.17        | 11.39         |
| h3                       | 0.8.6   | ✗      | 63302.8    | 15.31        | 10.38         |
| h3-router                | 0.8.6   | ✓      | 63163.2    | 15.34        | 10.36         |
| bare                     | 10.13.0 | ✗      | 59366.4    | 16.35        | 10.59         |
| foxify                   | 0.10.20 | ✓      | 57925.6    | 16.77        | 9.50          |
| connect                  | 3.7.0   | ✗      | 56908.0    | 17.07        | 10.15         |
| polka                    | 0.5.2   | ✓      | 56853.6    | 17.09        | 10.14         |
| micro                    | 9.4.1   | ✗      | 54840.0    | 17.74        | 9.78          |
| restana                  | 4.9.7   | ✓      | 54340.8    | 17.89        | 9.69          |
| fastify                  | 4.24.3  | ✓      | 53352.0    | 18.24        | 9.57          |
| server-base-router       | 7.1.32  | ✓      | 53194.4    | 18.30        | 9.49          |
| server-base              | 7.1.32  | ✗      | 52887.2    | 18.40        | 9.43          |
| yeps                     | 1.1.1   | ✗      | 52120.8    | 18.69        | 9.30          |
| micro-route              | 2.5.0   | ✓      | 49883.2    | 19.55        | 8.90          |
| connect-router           | 1.3.8   | ✓      | 49536.0    | 19.69        | 8.83          |
| trek-engine              | 1.0.5   | ✗      | 47770.4    | 20.44        | 7.84          |
| trek-router              | 1.2.0   | ✓      | 46621.8    | 20.95        | 7.65          |
| vapr                     | 0.6.0   | ✓      | 45650.4    | 21.40        | 7.49          |
| yeps-router              | 1.2.0   | ✓      | 43325.6    | 22.58        | 7.73          |
| spirit                   | 0.6.1   | ✗      | 41802.4    | 23.39        | 7.46          |
| koa                      | 2.14.2  | ✗      | 41794.4    | 23.43        | 7.45          |
| spirit-router            | 0.5.0   | ✓      | 41363.2    | 23.66        | 7.38          |
| total.js                 | 3.4.13  | ✓      | 39395.2    | 24.88        | 12.06         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38927.2    | 25.19        | 6.94          |
| take-five                | 2.0.0   | ✓      | 38894.2    | 25.20        | 13.98         |
| restify                  | 8.6.1   | ✓      | 38823.4    | 25.27        | 7.00          |
| koa-router               | 12.0.1  | ✓      | 36539.4    | 26.87        | 6.52          |
| hapi                     | 20.3.0  | ✓      | 34042.2    | 28.87        | 6.07          |
| microrouter              | 3.1.3   | ✓      | 32007.4    | 30.74        | 5.71          |
| trpc-router              | 9.27.3  | ✓      | 26832.0    | 36.77        | 5.94          |
| egg.js                   | 3.17.5  | ✓      | 17622.9    | 56.22        | 6.30          |
| express                  | 4.18.2  | ✓      | 13580.6    | 73.08        | 2.42          |
| fastify-big-json         | 4.24.3  | ✓      | 12987.2    | 76.46        | 149.43        |
| express-with-middlewares | 4.18.2  | ✓      | 12643.4    | 78.53        | 4.70          |
| express-route-prefix     | 4.18.2  | ✓      | 11050.6    | 89.91        | 4.09          |
| rayo                     | 1.4.5   | ✓      | N/A        | N/A          | N/A           |

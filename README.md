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
* __Run:__ Mon Jan 22 2024 02:16:18 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 66616.8    | 14.52        | 11.88         |
| h3                       | 0.8.6   | ✗      | 65312.0    | 14.80        | 10.71         |
| 0http                    | 3.5.2   | ✓      | 64157.6    | 15.10        | 11.44         |
| h3-router                | 0.8.6   | ✓      | 62354.4    | 15.55        | 10.23         |
| bare                     | 10.13.0 | ✗      | 59052.0    | 16.44        | 10.53         |
| foxify                   | 0.10.20 | ✓      | 58829.6    | 16.49        | 9.65          |
| polka                    | 0.5.2   | ✓      | 56544.0    | 17.19        | 10.08         |
| fastify                  | 4.25.2  | ✓      | 56398.4    | 17.23        | 10.11         |
| connect                  | 3.7.0   | ✗      | 56371.2    | 17.24        | 10.05         |
| restana                  | 4.9.7   | ✓      | 55310.4    | 17.58        | 9.86          |
| micro                    | 9.4.1   | ✗      | 54665.6    | 17.80        | 9.75          |
| server-base              | 7.1.32  | ✗      | 53632.0    | 18.15        | 9.56          |
| server-base-router       | 7.1.32  | ✓      | 53398.4    | 18.23        | 9.52          |
| yeps                     | 1.1.1   | ✗      | 52462.4    | 18.56        | 9.36          |
| micro-route              | 2.5.0   | ✓      | 49912.0    | 19.55        | 8.90          |
| connect-router           | 1.3.8   | ✓      | 49893.6    | 19.55        | 8.90          |
| trek-engine              | 1.0.5   | ✗      | 47699.2    | 20.47        | 7.82          |
| trek-router              | 1.2.0   | ✓      | 47285.6    | 20.65        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 45365.6    | 21.54        | 7.44          |
| yeps-router              | 1.2.0   | ✓      | 44064.0    | 22.19        | 7.86          |
| spirit                   | 0.6.1   | ✗      | 42716.0    | 22.90        | 7.62          |
| koa                      | 2.15.0  | ✗      | 42507.2    | 23.02        | 7.58          |
| spirit-router            | 0.5.0   | ✓      | 42090.4    | 23.31        | 7.51          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40316.8    | 24.31        | 7.19          |
| total.js                 | 3.4.13  | ✓      | 38759.4    | 25.30        | 11.87         |
| restify                  | 8.6.1   | ✓      | 38723.0    | 25.33        | 6.98          |
| take-five                | 2.0.0   | ✓      | 37912.2    | 25.88        | 13.63         |
| koa-router               | 12.0.1  | ✓      | 36967.0    | 26.55        | 6.59          |
| hapi                     | 20.3.0  | ✓      | 33913.4    | 28.98        | 6.05          |
| microrouter              | 3.1.3   | ✓      | 32359.4    | 30.40        | 5.77          |
| trpc-router              | 9.27.4  | ✓      | 26630.0    | 37.04        | 5.89          |
| egg.js                   | 3.18.0  | ✓      | 17332.0    | 57.18        | 6.20          |
| express                  | 4.18.2  | ✓      | 13329.0    | 74.48        | 2.38          |
| fastify-big-json         | 4.25.2  | ✓      | 12972.6    | 76.56        | 149.26        |
| express-with-middlewares | 4.18.2  | ✓      | 12418.2    | 79.97        | 4.62          |
| express-route-prefix     | 4.18.2  | ✓      | 10969.2    | 90.58        | 4.06          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

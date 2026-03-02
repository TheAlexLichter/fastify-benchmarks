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
* __Run:__ Mon Mar 02 2026 03:37:48 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 66927.6    | 14.45        | 11.94         |
| polkadot                 | 1.0.0   | ✗      | 66414.4    | 14.56        | 11.84         |
| h3                       | 0.8.6   | ✗      | 62726.4    | 15.42        | 10.29         |
| h3-router                | 0.8.6   | ✓      | 62605.6    | 15.46        | 10.27         |
| restana                  | 4.9.9   | ✓      | 61128.8    | 15.89        | 10.90         |
| foxify                   | 0.10.20 | ✓      | 60081.6    | 16.15        | 9.85          |
| bare                     | 10.13.0 | ✗      | 58754.4    | 16.52        | 10.48         |
| polka                    | 0.5.2   | ✓      | 58202.4    | 16.68        | 10.38         |
| connect                  | 3.7.0   | ✗      | 56568.8    | 17.18        | 10.09         |
| micro                    | 9.4.1   | ✗      | 56044.0    | 17.35        | 9.99          |
| fastify                  | 4.29.1  | ✓      | 55898.4    | 17.39        | 10.02         |
| server-base              | 7.1.32  | ✗      | 55720.0    | 17.44        | 9.94          |
| server-base-router       | 7.1.32  | ✓      | 54168.8    | 17.97        | 9.66          |
| yeps                     | 1.1.1   | ✗      | 52112.8    | 18.69        | 9.29          |
| connect-router           | 1.3.8   | ✓      | 50432.8    | 19.33        | 8.99          |
| micro-route              | 2.5.0   | ✓      | 50144.8    | 19.45        | 8.94          |
| trek-engine              | 1.0.5   | ✗      | 49320.8    | 19.78        | 8.09          |
| trek-router              | 1.2.0   | ✓      | 48384.0    | 20.17        | 7.94          |
| vapr                     | 0.6.0   | ✓      | 45857.6    | 21.30        | 7.52          |
| spirit-router            | 0.5.0   | ✓      | 44232.0    | 22.08        | 7.89          |
| yeps-router              | 1.2.0   | ✓      | 43140.0    | 22.68        | 7.69          |
| koa                      | 2.16.4  | ✗      | 42074.4    | 23.26        | 7.50          |
| spirit                   | 0.6.1   | ✗      | 41483.2    | 23.62        | 7.40          |
| total.js                 | 3.4.13  | ✓      | 39748.8    | 24.66        | 12.17         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39369.4    | 24.90        | 7.02          |
| restify                  | 8.6.1   | ✓      | 39130.6    | 25.06        | 7.05          |
| take-five                | 2.0.0   | ✓      | 39018.6    | 25.13        | 14.03         |
| koa-router               | 12.0.1  | ✓      | 36644.6    | 26.79        | 6.53          |
| hapi                     | 20.3.0  | ✓      | 32454.0    | 30.31        | 5.79          |
| microrouter              | 3.1.3   | ✓      | 31475.6    | 31.28        | 5.61          |
| trpc-router              | 9.27.4  | ✓      | 27244.4    | 36.20        | 6.03          |
| egg.js                   | 3.34.0  | ✓      | 16672.1    | 59.46        | 5.96          |
| express                  | 4.22.1  | ✓      | 13269.8    | 74.82        | 2.37          |
| fastify-big-json         | 4.29.1  | ✓      | 12726.0    | 78.02        | 146.41        |
| express-with-middlewares | 4.22.1  | ✓      | 12378.6    | 80.23        | 4.60          |
| express-route-prefix     | 4.22.1  | ✓      | 10673.0    | 93.12        | 3.95          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

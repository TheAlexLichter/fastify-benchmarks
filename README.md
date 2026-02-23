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
* __Run:__ Mon Feb 23 2026 03:43:26 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 69998.0    | 13.79        | 12.48         |
| h3                       | 0.8.6   | ✗      | 67680.0    | 14.30        | 11.10         |
| 0http                    | 3.5.3   | ✓      | 67298.0    | 14.36        | 12.00         |
| h3-router                | 0.8.6   | ✓      | 64347.2    | 15.03        | 10.56         |
| bare                     | 10.13.0 | ✗      | 60715.2    | 15.98        | 10.83         |
| restana                  | 4.9.9   | ✓      | 60644.0    | 16.02        | 10.82         |
| foxify                   | 0.10.20 | ✓      | 60241.6    | 16.10        | 9.88          |
| polka                    | 0.5.2   | ✓      | 58385.6    | 16.62        | 10.41         |
| connect                  | 3.7.0   | ✗      | 56744.0    | 17.13        | 10.12         |
| fastify                  | 4.29.1  | ✓      | 56542.4    | 17.19        | 10.14         |
| micro                    | 9.4.1   | ✗      | 56181.6    | 17.30        | 10.02         |
| server-base              | 7.1.32  | ✗      | 54095.2    | 18.00        | 9.65          |
| server-base-router       | 7.1.32  | ✓      | 52713.6    | 18.47        | 9.40          |
| yeps                     | 1.1.1   | ✗      | 52202.4    | 18.67        | 9.31          |
| connect-router           | 1.3.8   | ✓      | 51144.0    | 19.05        | 9.12          |
| micro-route              | 2.5.0   | ✓      | 49043.2    | 19.88        | 8.75          |
| trek-engine              | 1.0.5   | ✗      | 48534.4    | 20.11        | 7.96          |
| trek-router              | 1.2.0   | ✓      | 47798.4    | 20.41        | 7.84          |
| vapr                     | 0.6.0   | ✓      | 45940.0    | 21.26        | 7.54          |
| yeps-router              | 1.2.0   | ✓      | 43823.2    | 22.32        | 7.82          |
| spirit-router            | 0.5.0   | ✓      | 43387.2    | 22.53        | 7.74          |
| spirit                   | 0.6.1   | ✗      | 42400.8    | 23.09        | 7.56          |
| koa                      | 2.16.3  | ✗      | 41880.0    | 23.36        | 7.47          |
| total.js                 | 3.4.13  | ✓      | 40084.8    | 24.44        | 12.27         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39121.4    | 25.05        | 6.98          |
| restify                  | 8.6.1   | ✓      | 39048.2    | 25.10        | 7.04          |
| take-five                | 2.0.0   | ✓      | 38852.2    | 25.23        | 13.97         |
| koa-router               | 12.0.1  | ✓      | 36791.4    | 26.68        | 6.56          |
| hapi                     | 20.3.0  | ✓      | 32823.2    | 29.95        | 5.85          |
| microrouter              | 3.1.3   | ✓      | 31982.4    | 30.76        | 5.70          |
| trpc-router              | 9.27.4  | ✓      | 26979.6    | 36.56        | 5.97          |
| egg.js                   | 3.34.0  | ✓      | 16965.5    | 58.43        | 6.07          |
| express                  | 4.22.1  | ✓      | 13524.6    | 73.37        | 2.41          |
| fastify-big-json         | 4.29.1  | ✓      | 12728.4    | 78.03        | 146.45        |
| express-with-middlewares | 4.22.1  | ✓      | 12380.8    | 80.21        | 4.60          |
| express-route-prefix     | 4.22.1  | ✓      | 10821.4    | 91.81        | 4.00          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

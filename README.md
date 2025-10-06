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
* __Run:__ Mon Oct 06 2025 02:46:56 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68791.6    | 14.03        | 12.27         |
| polkadot                 | 1.0.0   | ✗      | 66353.6    | 14.58        | 11.83         |
| h3-router                | 0.8.6   | ✓      | 65627.2    | 14.75        | 10.76         |
| h3                       | 0.8.6   | ✗      | 64164.0    | 15.12        | 10.52         |
| restana                  | 4.9.9   | ✓      | 61816.8    | 15.68        | 11.02         |
| foxify                   | 0.10.20 | ✓      | 60750.4    | 15.97        | 9.97          |
| bare                     | 10.13.0 | ✗      | 60030.4    | 16.16        | 10.71         |
| polka                    | 0.5.2   | ✓      | 58919.2    | 16.47        | 10.51         |
| micro                    | 9.4.1   | ✗      | 57577.6    | 16.87        | 10.27         |
| connect                  | 3.7.0   | ✗      | 57473.6    | 16.91        | 10.25         |
| fastify                  | 4.29.1  | ✓      | 55956.0    | 17.37        | 10.03         |
| server-base-router       | 7.1.32  | ✓      | 55531.2    | 17.51        | 9.90          |
| server-base              | 7.1.32  | ✗      | 54955.2    | 17.70        | 9.80          |
| yeps                     | 1.1.1   | ✗      | 52208.0    | 18.66        | 9.31          |
| connect-router           | 1.3.8   | ✓      | 51320.0    | 18.98        | 9.15          |
| micro-route              | 2.5.0   | ✓      | 49852.8    | 19.56        | 8.89          |
| trek-engine              | 1.0.5   | ✗      | 48504.0    | 20.12        | 7.96          |
| trek-router              | 1.2.0   | ✓      | 46829.6    | 20.86        | 7.68          |
| vapr                     | 0.6.0   | ✓      | 46020.0    | 21.22        | 7.55          |
| yeps-router              | 1.2.0   | ✓      | 44286.4    | 22.08        | 7.90          |
| spirit-router            | 0.5.0   | ✓      | 44100.0    | 22.19        | 7.87          |
| spirit                   | 0.6.1   | ✗      | 43369.6    | 22.56        | 7.73          |
| koa                      | 2.16.2  | ✗      | 42347.2    | 23.12        | 7.55          |
| total.js                 | 3.4.13  | ✓      | 40160.8    | 24.41        | 12.29         |
| restify                  | 8.6.1   | ✓      | 39557.6    | 24.78        | 7.13          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39279.0    | 24.96        | 7.01          |
| take-five                | 2.0.0   | ✓      | 38837.0    | 25.25        | 13.96         |
| koa-router               | 12.0.1  | ✓      | 36593.0    | 26.83        | 6.53          |
| hapi                     | 20.3.0  | ✓      | 33744.8    | 29.13        | 6.02          |
| microrouter              | 3.1.3   | ✓      | 32251.0    | 30.51        | 5.75          |
| trpc-router              | 9.27.4  | ✓      | 27384.4    | 36.01        | 6.06          |
| egg.js                   | 3.31.0  | ✓      | 16764.8    | 59.11        | 6.00          |
| express                  | 4.21.2  | ✓      | 13538.0    | 73.30        | 2.41          |
| fastify-big-json         | 4.29.1  | ✓      | 12959.2    | 76.63        | 149.09        |
| express-with-middlewares | 4.21.2  | ✓      | 12402.8    | 80.07        | 4.61          |
| express-route-prefix     | 4.21.2  | ✓      | 10891.5    | 91.22        | 4.03          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

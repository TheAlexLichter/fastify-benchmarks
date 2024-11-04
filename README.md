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
* __Run:__ Mon Nov 04 2024 02:41:05 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| h3                       | 0.8.6   | ✗      | 65294.0    | 14.82        | 10.71         |
| 0http                    | 3.5.3   | ✓      | 65216.8    | 14.84        | 11.63         |
| polkadot                 | 1.0.0   | ✗      | 64881.6    | 14.91        | 11.57         |
| h3-router                | 0.8.6   | ✓      | 64215.2    | 15.08        | 10.53         |
| restana                  | 4.9.9   | ✓      | 59740.0    | 16.24        | 10.65         |
| polka                    | 0.5.2   | ✓      | 59171.2    | 16.40        | 10.55         |
| foxify                   | 0.10.20 | ✓      | 58030.4    | 16.73        | 9.52          |
| micro                    | 9.4.1   | ✗      | 57679.2    | 16.84        | 10.28         |
| bare                     | 10.13.0 | ✗      | 57070.4    | 17.03        | 10.18         |
| server-base              | 7.1.32  | ✗      | 56075.2    | 17.34        | 10.00         |
| server-base-router       | 7.1.32  | ✓      | 55436.0    | 17.54        | 9.89          |
| fastify                  | 4.28.1  | ✓      | 55084.0    | 17.66        | 9.88          |
| connect                  | 3.7.0   | ✗      | 54181.6    | 17.97        | 9.66          |
| yeps                     | 1.1.1   | ✗      | 53944.0    | 18.04        | 9.62          |
| micro-route              | 2.5.0   | ✓      | 51192.0    | 19.04        | 9.13          |
| connect-router           | 1.3.8   | ✓      | 48576.8    | 20.09        | 8.66          |
| trek-engine              | 1.0.5   | ✗      | 47232.8    | 20.67        | 7.75          |
| vapr                     | 0.6.0   | ✓      | 47049.6    | 20.76        | 7.72          |
| trek-router              | 1.2.0   | ✓      | 46116.0    | 21.19        | 7.56          |
| spirit                   | 0.6.1   | ✗      | 45008.8    | 21.71        | 8.03          |
| spirit-router            | 0.5.0   | ✓      | 44946.4    | 21.76        | 8.02          |
| yeps-router              | 1.2.0   | ✓      | 43571.2    | 22.45        | 7.77          |
| koa                      | 2.15.3  | ✗      | 42765.6    | 22.88        | 7.63          |
| total.js                 | 3.4.13  | ✓      | 40541.6    | 24.16        | 12.41         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40079.2    | 24.46        | 7.15          |
| restify                  | 8.6.1   | ✓      | 39167.0    | 25.03        | 7.06          |
| take-five                | 2.0.0   | ✓      | 39074.2    | 25.10        | 14.05         |
| koa-router               | 12.0.1  | ✓      | 38531.0    | 25.44        | 6.87          |
| hapi                     | 20.3.0  | ✓      | 33410.4    | 29.41        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 32026.4    | 30.71        | 5.71          |
| trpc-router              | 9.27.4  | ✓      | 26348.8    | 37.44        | 5.83          |
| egg.js                   | 3.28.0  | ✓      | 17218.3    | 57.55        | 6.16          |
| express                  | 4.21.1  | ✓      | 13202.8    | 75.20        | 2.35          |
| fastify-big-json         | 4.28.1  | ✓      | 12777.8    | 77.71        | 147.02        |
| express-with-middlewares | 4.21.1  | ✓      | 12541.4    | 79.20        | 4.66          |
| express-route-prefix     | 4.21.1  | ✓      | 10736.6    | 92.56        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

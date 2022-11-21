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
* __Node:__ `v14.20.1`
* __Run:__ Mon Nov 21 2022 02:55:53 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 48822.4    | 19.99        | 8.71          |
| foxify                   | 0.10.20 | ✓      | 48388.8    | 20.17        | 7.94          |
| polkadot                 | 1.0.0   | ✗      | 48293.6    | 20.22        | 8.61          |
| connect                  | 3.7.0   | ✗      | 47385.6    | 20.61        | 8.45          |
| polka                    | 0.5.2   | ✓      | 46328.8    | 21.10        | 8.26          |
| 0http                    | 3.4.1   | ✓      | 45820.0    | 21.34        | 8.17          |
| server-base-router       | 7.1.32  | ✓      | 45747.2    | 21.36        | 8.16          |
| micro                    | 9.4.1   | ✗      | 45692.8    | 21.39        | 8.15          |
| server-base              | 7.1.32  | ✗      | 45088.8    | 21.68        | 8.04          |
| fastify                  | 4.10.0  | ✓      | 44402.4    | 22.03        | 7.96          |
| h3-router                | 0.8.6   | ✓      | 43991.2    | 22.24        | 7.22          |
| h3                       | 0.8.6   | ✗      | 43309.6    | 22.60        | 7.10          |
| connect-router           | 1.3.7   | ✓      | 43104.8    | 22.71        | 7.69          |
| yeps                     | 1.1.1   | ✗      | 42856.8    | 22.83        | 7.64          |
| restana                  | 4.9.6   | ✓      | 41404.0    | 23.66        | 7.38          |
| micro-route              | 2.5.0   | ✓      | 40717.8    | 24.06        | 7.26          |
| trek-router              | 1.2.0   | ✓      | 38249.4    | 25.64        | 6.27          |
| trek-engine              | 1.0.5   | ✗      | 37280.6    | 26.35        | 6.12          |
| vapr                     | 0.6.0   | ✓      | 36973.0    | 26.54        | 6.06          |
| yeps-router              | 1.2.0   | ✓      | 35235.8    | 27.89        | 6.28          |
| koa                      | 2.13.4  | ✗      | 33482.8    | 29.38        | 5.97          |
| spirit                   | 0.6.1   | ✗      | 33325.6    | 29.54        | 5.94          |
| spirit-router            | 0.5.0   | ✓      | 32210.2    | 30.57        | 5.74          |
| total.js                 | 3.4.13  | ✓      | 31430.8    | 31.32        | 9.62          |
| take-five                | 2.0.0   | ✓      | 30953.6    | 31.82        | 11.13         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 30528.4    | 32.27        | 5.44          |
| restify                  | 8.6.1   | ✓      | 30136.4    | 32.68        | 5.43          |
| koa-router               | 12.0.0  | ✓      | 28097.2    | 35.11        | 5.01          |
| hapi                     | 20.2.2  | ✓      | 24768.0    | 39.88        | 4.42          |
| microrouter              | 3.1.3   | ✓      | 24307.2    | 40.64        | 4.33          |
| trpc-router              | 9.27.4  | ✓      | 20572.8    | 48.09        | 4.55          |
| egg.js                   | 3.5.0   | ✓      | 15172.8    | 65.38        | 5.43          |
| express                  | 4.18.2  | ✓      | 10152.0    | 97.94        | 1.81          |
| express-with-middlewares | 4.18.2  | ✓      | 8609.8     | 115.52       | 3.20          |
| express-route-prefix     | 4.18.2  | ✓      | 8468.0     | 117.54       | 3.13          |
| fastify-big-json         | 4.10.0  | ✓      | 8347.1     | 119.29       | 96.04         |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

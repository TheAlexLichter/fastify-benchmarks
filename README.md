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
* __Run:__ Mon Aug 03 2026 04:31:57 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 133967.2   | 7.05         | 23.89         |
| connect                  | 3.7.0   | ✗      | 133328.8   | 7.07         | 23.78         |
| polka                    | 0.5.2   | ✓      | 130679.2   | 7.18         | 23.30         |
| 0http                    | 3.5.3   | ✓      | 130048.0   | 7.19         | 23.19         |
| polkadot                 | 1.0.0   | ✗      | 126270.4   | 7.43         | 22.52         |
| fastify                  | 4.29.1  | ✓      | 126135.2   | 7.45         | 22.62         |
| foxify                   | 0.10.20 | ✓      | 124456.0   | 7.54         | 20.42         |
| micro                    | 9.4.1   | ✗      | 122435.2   | 7.68         | 21.83         |
| restana                  | 4.9.9   | ✓      | 120752.0   | 7.79         | 21.53         |
| h3                       | 0.8.6   | ✗      | 120104.0   | 7.83         | 19.70         |
| yeps                     | 1.1.1   | ✗      | 118846.4   | 7.93         | 21.20         |
| server-base              | 7.1.32  | ✗      | 116419.2   | 8.09         | 20.76         |
| h3-router                | 0.8.6   | ✓      | 116100.8   | 8.11         | 19.04         |
| server-base-router       | 7.1.32  | ✓      | 114102.4   | 8.26         | 20.35         |
| connect-router           | 1.3.8   | ✓      | 111161.6   | 8.50         | 19.82         |
| micro-route              | 2.5.0   | ✓      | 110484.8   | 8.56         | 19.70         |
| trek-engine              | 1.0.5   | ✗      | 103624.0   | 9.15         | 17.00         |
| vapr                     | 0.6.0   | ✓      | 98315.2    | 9.67         | 16.13         |
| trek-router              | 1.2.0   | ✓      | 96502.4    | 9.87         | 15.83         |
| yeps-router              | 1.2.0   | ✓      | 91124.8    | 10.48        | 16.25         |
| take-five                | 2.0.0   | ✓      | 85576.0    | 11.19        | 30.77         |
| koa                      | 2.16.4  | ✗      | 84796.8    | 11.30        | 15.12         |
| total.js                 | 3.4.13  | ✓      | 84550.4    | 11.33        | 25.88         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 77953.6    | 12.33        | 13.90         |
| restify                  | 8.6.1   | ✓      | 76657.6    | 12.55        | 13.82         |
| koa-router               | 12.0.1  | ✓      | 74309.2    | 12.96        | 13.25         |
| spirit                   | 0.6.1   | ✗      | 65879.2    | 14.68        | 11.75         |
| microrouter              | 3.1.3   | ✓      | 63707.6    | 15.20        | 11.36         |
| hapi                     | 20.3.0  | ✓      | 63366.8    | 15.28        | 11.30         |
| spirit-router            | 0.5.0   | ✓      | 61976.8    | 15.64        | 11.05         |
| trpc-router              | 9.27.4  | ✓      | 52951.2    | 18.38        | 11.72         |
| egg.js                   | 3.34.0  | ✓      | 30904.2    | 31.85        | 11.05         |
| express                  | 4.22.2  | ✓      | 26441.2    | 37.30        | 4.72          |
| express-with-middlewares | 4.22.2  | ✓      | 23165.6    | 42.66        | 8.62          |
| fastify-big-json         | 4.29.1  | ✓      | 18631.3    | 53.16        | 214.37        |
| express-route-prefix     | 4.22.2  | ✓      | 18397.7    | 53.83        | 6.81          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

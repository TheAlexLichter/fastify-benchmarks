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
* __Run:__ Mon Jun 15 2026 06:08:30 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 70326.8    | 13.73        | 12.54         |
| polkadot                 | 1.0.0   | ✗      | 70038.8    | 13.79        | 12.49         |
| polka                    | 0.5.2   | ✓      | 69636.4    | 13.87        | 12.42         |
| 0http                    | 3.5.3   | ✓      | 69388.4    | 13.92        | 12.37         |
| h3                       | 0.8.6   | ✗      | 68985.2    | 13.99        | 11.32         |
| connect                  | 3.7.0   | ✗      | 68370.4    | 14.13        | 12.19         |
| foxify                   | 0.10.20 | ✓      | 68355.6    | 14.13        | 11.21         |
| h3-router                | 0.8.6   | ✓      | 66454.8    | 14.56        | 10.90         |
| fastify                  | 4.29.1  | ✓      | 66085.2    | 14.64        | 11.85         |
| yeps                     | 1.1.1   | ✗      | 65311.6    | 14.81        | 11.65         |
| restana                  | 4.9.9   | ✓      | 64735.2    | 14.99        | 11.54         |
| micro                    | 9.4.1   | ✗      | 62721.2    | 15.44        | 11.19         |
| connect-router           | 1.3.8   | ✓      | 62637.6    | 15.46        | 11.17         |
| server-base              | 7.1.32  | ✗      | 62614.0    | 15.48        | 11.17         |
| micro-route              | 2.5.0   | ✓      | 62274.4    | 15.56        | 11.11         |
| server-base-router       | 7.1.32  | ✓      | 61580.0    | 15.74        | 10.98         |
| vapr                     | 0.6.0   | ✓      | 57217.6    | 16.98        | 9.39          |
| trek-engine              | 1.0.5   | ✗      | 53755.2    | 18.10        | 8.82          |
| yeps-router              | 1.2.0   | ✓      | 53115.2    | 18.33        | 9.47          |
| trek-router              | 1.2.0   | ✓      | 51098.4    | 19.07        | 8.38          |
| koa                      | 2.16.4  | ✗      | 49598.4    | 19.66        | 8.85          |
| take-five                | 2.0.0   | ✓      | 48553.6    | 20.10        | 17.46         |
| total.js                 | 3.4.13  | ✓      | 47266.4    | 20.66        | 14.47         |
| restify                  | 8.6.1   | ✓      | 47245.6    | 20.67        | 8.52          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 45982.4    | 21.25        | 8.20          |
| koa-router               | 12.0.1  | ✓      | 43238.4    | 22.63        | 7.71          |
| microrouter              | 3.1.3   | ✓      | 40527.2    | 24.18        | 7.23          |
| hapi                     | 20.3.0  | ✓      | 38834.6    | 25.25        | 6.93          |
| spirit                   | 0.6.1   | ✗      | 37753.6    | 25.99        | 6.73          |
| spirit-router            | 0.5.0   | ✓      | 31169.0    | 31.59        | 5.56          |
| trpc-router              | 9.27.4  | ✓      | 29396.8    | 33.51        | 6.50          |
| egg.js                   | 3.34.0  | ✓      | 18860.1    | 52.50        | 6.75          |
| express                  | 4.22.2  | ✓      | 15895.8    | 62.37        | 2.83          |
| express-with-middlewares | 4.22.2  | ✓      | 15022.8    | 66.02        | 5.59          |
| fastify-big-json         | 4.29.1  | ✓      | 13004.0    | 76.35        | 149.61        |
| express-route-prefix     | 4.22.2  | ✓      | 11858.2    | 83.76        | 4.39          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

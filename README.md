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
* __Run:__ Mon May 04 2026 04:47:44 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 71385.2    | 13.52        | 12.73         |
| 0http                    | 3.5.3   | ✓      | 69894.8    | 13.81        | 12.46         |
| h3                       | 0.8.6   | ✗      | 64266.0    | 15.07        | 10.54         |
| h3-router                | 0.8.6   | ✓      | 63597.2    | 15.23        | 10.43         |
| restana                  | 4.9.9   | ✓      | 60911.2    | 15.94        | 10.86         |
| bare                     | 10.13.0 | ✗      | 60360.8    | 16.07        | 10.76         |
| foxify                   | 0.10.20 | ✓      | 59654.4    | 16.26        | 9.78          |
| polka                    | 0.5.2   | ✓      | 58532.0    | 16.58        | 10.44         |
| connect                  | 3.7.0   | ✗      | 58088.0    | 16.71        | 10.36         |
| fastify                  | 4.29.1  | ✓      | 57597.6    | 16.86        | 10.33         |
| micro                    | 9.4.1   | ✗      | 57430.4    | 16.91        | 10.24         |
| server-base              | 7.1.32  | ✗      | 56576.0    | 17.17        | 10.09         |
| server-base-router       | 7.1.32  | ✓      | 55265.6    | 17.59        | 9.86          |
| connect-router           | 1.3.8   | ✓      | 51642.4    | 18.88        | 9.21          |
| yeps                     | 1.1.1   | ✗      | 51205.6    | 19.04        | 9.13          |
| micro-route              | 2.5.0   | ✓      | 50648.8    | 19.25        | 9.03          |
| trek-engine              | 1.0.5   | ✗      | 48556.8    | 20.10        | 7.96          |
| trek-router              | 1.2.0   | ✓      | 48320.0    | 20.20        | 7.93          |
| vapr                     | 0.6.0   | ✓      | 46150.4    | 21.17        | 7.57          |
| spirit                   | 0.6.1   | ✗      | 45587.2    | 21.44        | 8.13          |
| spirit-router            | 0.5.0   | ✓      | 44367.2    | 22.03        | 7.91          |
| yeps-router              | 1.2.0   | ✓      | 43985.6    | 22.23        | 7.84          |
| koa                      | 2.16.4  | ✗      | 42233.6    | 23.18        | 7.53          |
| total.js                 | 3.4.13  | ✓      | 40269.8    | 24.33        | 12.33         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39976.0    | 24.51        | 7.13          |
| restify                  | 8.6.1   | ✓      | 39809.0    | 24.63        | 7.17          |
| take-five                | 2.0.0   | ✓      | 39509.8    | 24.81        | 14.21         |
| koa-router               | 12.0.1  | ✓      | 37518.6    | 26.15        | 6.69          |
| hapi                     | 20.3.0  | ✓      | 32972.0    | 29.83        | 5.88          |
| microrouter              | 3.1.3   | ✓      | 31702.8    | 31.05        | 5.65          |
| trpc-router              | 9.27.4  | ✓      | 27837.2    | 35.41        | 6.16          |
| egg.js                   | 3.34.0  | ✓      | 17600.6    | 56.30        | 6.29          |
| express                  | 4.22.1  | ✓      | 13302.2    | 74.62        | 2.37          |
| express-with-middlewares | 4.22.1  | ✓      | 12626.4    | 78.64        | 4.70          |
| fastify-big-json         | 4.29.1  | ✓      | 12464.2    | 79.69        | 143.41        |
| express-route-prefix     | 4.22.1  | ✓      | 10325.0    | 96.26        | 3.82          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

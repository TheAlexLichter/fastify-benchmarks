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
* __Run:__ Mon Dec 16 2024 02:51:39 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68455.2    | 14.11        | 12.21         |
| polkadot                 | 1.0.0   | ✗      | 64865.6    | 14.91        | 11.57         |
| h3                       | 0.8.6   | ✗      | 63806.0    | 15.19        | 10.47         |
| h3-router                | 0.8.6   | ✓      | 63586.0    | 15.23        | 10.43         |
| restana                  | 4.9.9   | ✓      | 60790.4    | 15.97        | 10.84         |
| bare                     | 10.13.0 | ✗      | 59703.2    | 16.25        | 10.65         |
| connect                  | 3.7.0   | ✗      | 58402.4    | 16.62        | 10.41         |
| foxify                   | 0.10.20 | ✓      | 57742.4    | 16.82        | 9.47          |
| polka                    | 0.5.2   | ✓      | 57362.4    | 16.93        | 10.23         |
| fastify                  | 4.29.0  | ✓      | 57302.4    | 16.96        | 10.27         |
| micro                    | 9.4.1   | ✗      | 55601.6    | 17.49        | 9.92          |
| server-base-router       | 7.1.32  | ✓      | 55414.4    | 17.54        | 9.88          |
| server-base              | 7.1.32  | ✗      | 55184.0    | 17.62        | 9.84          |
| yeps                     | 1.1.1   | ✗      | 51777.6    | 18.82        | 9.23          |
| connect-router           | 1.3.8   | ✓      | 50853.6    | 19.17        | 9.07          |
| micro-route              | 2.5.0   | ✓      | 50098.4    | 19.46        | 8.93          |
| trek-engine              | 1.0.5   | ✗      | 48876.8    | 19.97        | 8.02          |
| trek-router              | 1.2.0   | ✓      | 47362.4    | 20.62        | 7.77          |
| vapr                     | 0.6.0   | ✓      | 46939.2    | 20.81        | 7.70          |
| koa                      | 2.15.3  | ✗      | 42916.8    | 22.80        | 7.65          |
| yeps-router              | 1.2.0   | ✓      | 42633.6    | 22.96        | 7.60          |
| spirit                   | 0.6.1   | ✗      | 42365.6    | 23.13        | 7.56          |
| spirit-router            | 0.5.0   | ✓      | 40929.6    | 23.93        | 7.30          |
| total.js                 | 3.4.13  | ✓      | 40073.6    | 24.45        | 12.27         |
| take-five                | 2.0.0   | ✓      | 39931.4    | 24.55        | 14.36         |
| restify                  | 8.6.1   | ✓      | 39464.8    | 24.84        | 7.11          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39409.0    | 24.88        | 7.03          |
| koa-router               | 12.0.1  | ✓      | 37404.6    | 26.24        | 6.67          |
| hapi                     | 20.3.0  | ✓      | 34170.4    | 28.76        | 6.09          |
| microrouter              | 3.1.3   | ✓      | 32064.4    | 30.68        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 25417.6    | 38.83        | 5.62          |
| egg.js                   | 3.29.0  | ✓      | 17611.7    | 56.27        | 6.30          |
| express                  | 4.21.2  | ✓      | 14453.0    | 68.65        | 2.58          |
| fastify-big-json         | 4.29.0  | ✓      | 12692.6    | 78.24        | 146.02        |
| express-with-middlewares | 4.21.2  | ✓      | 12551.8    | 79.10        | 4.67          |
| express-route-prefix     | 4.21.2  | ✓      | 11122.6    | 89.34        | 4.12          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

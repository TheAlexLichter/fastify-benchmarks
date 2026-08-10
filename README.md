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
* __Run:__ Mon Aug 10 2026 03:14:24 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 115948.8   | 8.13         | 20.68         |
| 0http                    | 3.5.3   | ✓      | 115811.2   | 8.13         | 20.65         |
| connect                  | 3.7.0   | ✗      | 113116.8   | 8.35         | 20.17         |
| polka                    | 0.5.2   | ✓      | 109025.6   | 8.68         | 19.44         |
| server-base              | 7.1.32  | ✗      | 107862.4   | 8.77         | 19.24         |
| restana                  | 4.9.9   | ✓      | 107131.2   | 8.84         | 19.11         |
| fastify                  | 4.29.1  | ✓      | 106830.4   | 8.86         | 19.15         |
| yeps                     | 1.1.1   | ✗      | 105262.4   | 9.00         | 18.77         |
| foxify                   | 0.10.20 | ✓      | 104209.6   | 9.10         | 17.09         |
| server-base-router       | 7.1.32  | ✓      | 103752.0   | 9.14         | 18.50         |
| h3                       | 0.8.6   | ✗      | 103476.8   | 9.18         | 16.97         |
| micro                    | 9.4.1   | ✗      | 103230.4   | 9.19         | 18.41         |
| connect-router           | 1.3.8   | ✓      | 102857.6   | 9.23         | 18.34         |
| polkadot                 | 1.0.0   | ✗      | 102041.6   | 9.32         | 18.20         |
| h3-router                | 0.8.6   | ✓      | 100148.8   | 9.48         | 16.43         |
| micro-route              | 2.5.0   | ✓      | 99643.2    | 9.54         | 17.77         |
| trek-engine              | 1.0.5   | ✗      | 89928.0    | 10.62        | 14.75         |
| trek-router              | 1.2.0   | ✓      | 88747.2    | 10.77        | 14.56         |
| vapr                     | 0.6.0   | ✓      | 88664.0    | 10.78        | 14.54         |
| take-five                | 2.0.0   | ✓      | 80043.2    | 12.00        | 28.78         |
| total.js                 | 3.4.13  | ✓      | 77263.6    | 12.44        | 23.65         |
| yeps-router              | 1.2.0   | ✓      | 77241.6    | 12.45        | 13.78         |
| koa                      | 2.16.4  | ✗      | 72557.2    | 13.29        | 12.94         |
| restify                  | 8.6.1   | ✓      | 67579.2    | 14.30        | 12.18         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 66718.0    | 14.49        | 11.90         |
| spirit                   | 0.6.1   | ✗      | 66000.4    | 14.65        | 11.77         |
| koa-router               | 12.0.1  | ✓      | 65039.2    | 14.88        | 11.60         |
| spirit-router            | 0.5.0   | ✓      | 64119.2    | 15.10        | 11.43         |
| microrouter              | 3.1.3   | ✓      | 58299.2    | 16.65        | 10.40         |
| hapi                     | 20.3.0  | ✓      | 57676.0    | 16.84        | 10.29         |
| trpc-router              | 9.27.4  | ✓      | 46938.4    | 20.81        | 10.39         |
| egg.js                   | 3.34.0  | ✓      | 26479.2    | 37.26        | 9.47          |
| express                  | 4.22.2  | ✓      | 22617.2    | 43.70        | 4.03          |
| express-with-middlewares | 4.22.2  | ✓      | 20459.6    | 48.37        | 7.61          |
| fastify-big-json         | 4.29.1  | ✓      | 16437.3    | 60.31        | 189.13        |
| express-route-prefix     | 4.22.2  | ✓      | 15556.4    | 63.73        | 5.76          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

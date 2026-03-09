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
* __Run:__ Mon Mar 09 2026 03:41:40 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 72959.6    | 13.22        | 13.01         |
| bare                     | 10.13.0 | ✗      | 72945.2    | 13.21        | 13.01         |
| polkadot                 | 1.0.0   | ✗      | 72061.2    | 13.39        | 12.85         |
| polka                    | 0.5.2   | ✓      | 70368.4    | 13.72        | 12.55         |
| foxify                   | 0.10.20 | ✓      | 70248.4    | 13.74        | 11.52         |
| connect                  | 3.7.0   | ✗      | 69709.6    | 13.85        | 12.43         |
| restana                  | 4.9.9   | ✓      | 68688.4    | 14.08        | 12.25         |
| server-base-router       | 7.1.32  | ✓      | 67644.8    | 14.29        | 12.06         |
| yeps                     | 1.1.1   | ✗      | 66938.0    | 14.44        | 11.94         |
| server-base              | 7.1.32  | ✗      | 66838.8    | 14.46        | 11.92         |
| h3                       | 0.8.6   | ✗      | 66717.6    | 14.49        | 10.94         |
| fastify                  | 4.29.1  | ✓      | 66707.2    | 14.49        | 11.96         |
| h3-router                | 0.8.6   | ✓      | 66000.0    | 14.65        | 10.82         |
| connect-router           | 1.3.8   | ✓      | 64723.6    | 14.95        | 11.54         |
| micro                    | 9.4.1   | ✗      | 64308.0    | 15.05        | 11.47         |
| micro-route              | 2.5.0   | ✓      | 62523.2    | 15.50        | 11.15         |
| vapr                     | 0.6.0   | ✓      | 57580.8    | 16.87        | 9.45          |
| trek-engine              | 1.0.5   | ✗      | 55644.0    | 17.48        | 9.13          |
| trek-router              | 1.2.0   | ✓      | 52926.4    | 18.40        | 8.68          |
| yeps-router              | 1.2.0   | ✓      | 51896.0    | 18.77        | 9.25          |
| take-five                | 2.0.0   | ✓      | 51142.4    | 19.05        | 18.39         |
| total.js                 | 3.4.13  | ✓      | 50926.4    | 19.14        | 15.59         |
| koa                      | 2.16.4  | ✗      | 49708.0    | 19.62        | 8.87          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 46916.8    | 20.82        | 8.37          |
| restify                  | 8.6.1   | ✓      | 45484.8    | 21.49        | 8.20          |
| spirit                   | 0.6.1   | ✗      | 44694.4    | 21.93        | 7.97          |
| koa-router               | 12.0.1  | ✓      | 43798.4    | 22.33        | 7.81          |
| microrouter              | 3.1.3   | ✓      | 41168.0    | 23.79        | 7.34          |
| hapi                     | 20.3.0  | ✓      | 38934.6    | 25.18        | 6.94          |
| spirit-router            | 0.5.0   | ✓      | 36483.2    | 26.92        | 6.51          |
| trpc-router              | 9.27.4  | ✓      | 31353.6    | 31.39        | 6.94          |
| egg.js                   | 3.34.0  | ✓      | 18958.4    | 52.23        | 6.78          |
| express                  | 4.22.1  | ✓      | 16171.0    | 61.30        | 2.88          |
| express-with-middlewares | 4.22.1  | ✓      | 15017.4    | 66.05        | 5.59          |
| fastify-big-json         | 4.29.1  | ✓      | 12830.6    | 77.39        | 147.62        |
| express-route-prefix     | 4.22.1  | ✓      | 11929.4    | 83.27        | 4.41          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

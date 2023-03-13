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
* __Node:__ `v14.21.3`
* __Run:__ Mon Mar 13 2023 02:33:57 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| h3                       | 0.8.6   | ✗      | 30444.8    | 32.36        | 4.99          |
| micro                    | 9.4.1   | ✗      | 30256.8    | 32.56        | 5.40          |
| polka                    | 0.5.2   | ✓      | 29855.6    | 33.00        | 5.32          |
| foxify                   | 0.10.20 | ✓      | 29685.2    | 33.19        | 4.87          |
| h3-router                | 0.8.6   | ✓      | 29628.0    | 33.27        | 4.86          |
| polkadot                 | 1.0.0   | ✗      | 29350.0    | 33.60        | 5.23          |
| 0http                    | 3.5.1   | ✓      | 28338.4    | 34.82        | 5.05          |
| fastify                  | 4.14.1  | ✓      | 28102.4    | 35.08        | 5.04          |
| server-base              | 7.1.32  | ✗      | 27502.8    | 35.86        | 4.90          |
| bare                     | 10.13.0 | ✗      | 27459.2    | 35.93        | 4.90          |
| connect                  | 3.7.0   | ✗      | 26324.4    | 37.52        | 4.69          |
| server-base-router       | 7.1.32  | ✓      | 26191.6    | 37.67        | 4.67          |
| yeps                     | 1.1.1   | ✗      | 26178.0    | 37.69        | 4.67          |
| connect-router           | 1.3.8   | ✓      | 25610.4    | 38.55        | 4.57          |
| micro-route              | 2.5.0   | ✓      | 25574.0    | 38.62        | 4.56          |
| restana                  | 4.9.7   | ✓      | 25280.4    | 39.05        | 4.51          |
| trek-engine              | 1.0.5   | ✗      | 24852.1    | 39.74        | 4.08          |
| spirit-router            | 0.5.0   | ✓      | 24451.6    | 40.45        | 4.36          |
| spirit                   | 0.6.1   | ✗      | 24243.2    | 40.83        | 4.32          |
| trek-router              | 1.2.0   | ✓      | 23999.1    | 41.17        | 3.94          |
| yeps-router              | 1.2.0   | ✓      | 23061.2    | 42.85        | 4.11          |
| vapr                     | 0.6.0   | ✓      | 22889.7    | 43.19        | 3.75          |
| koa                      | 2.14.1  | ✗      | 21605.5    | 45.78        | 3.85          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 20001.9    | 49.50        | 3.57          |
| restify                  | 8.6.1   | ✓      | 19628.7    | 50.44        | 3.54          |
| total.js                 | 3.4.13  | ✓      | 19360.5    | 51.16        | 5.93          |
| take-five                | 2.0.0   | ✓      | 19315.5    | 51.26        | 6.94          |
| koa-router               | 12.0.0  | ✓      | 18890.7    | 52.42        | 3.37          |
| hapi                     | 20.3.0  | ✓      | 18238.3    | 54.31        | 3.25          |
| microrouter              | 3.1.3   | ✓      | 17217.7    | 57.54        | 3.07          |
| trpc-router              | 9.27.3  | ✓      | 16427.3    | 60.40        | 3.63          |
| egg.js                   | 3.15.0  | ✓      | 8802.2     | 113.04       | 3.15          |
| express                  | 4.18.2  | ✓      | 7380.8     | 134.85       | 1.32          |
| fastify-big-json         | 4.14.1  | ✓      | 6565.0     | 151.78       | 75.53         |
| express-with-middlewares | 4.18.2  | ✓      | 6147.9     | 161.89       | 2.29          |
| express-route-prefix     | 4.18.2  | ✓      | 6039.5     | 164.93       | 2.23          |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

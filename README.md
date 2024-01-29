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
* __Run:__ Mon Jan 29 2024 02:07:00 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| polkadot                 | 1.0.0   | ✗      | 65662.4    | 14.74        | 11.71         |
| h3-router                | 0.8.6   | ✓      | 60988.8    | 15.90        | 10.00         |
| h3                       | 0.8.6   | ✗      | 60576.0    | 16.01        | 9.94          |
| 0http                    | 3.5.2   | ✓      | 58190.4    | 16.70        | 10.38         |
| foxify                   | 0.10.20 | ✓      | 58069.6    | 16.72        | 9.53          |
| polka                    | 0.5.2   | ✓      | 56848.0    | 17.09        | 10.14         |
| bare                     | 10.13.0 | ✗      | 56418.4    | 17.23        | 10.06         |
| fastify                  | 4.25.2  | ✓      | 56113.6    | 17.32        | 10.06         |
| restana                  | 4.9.7   | ✓      | 55358.4    | 17.57        | 9.87          |
| micro                    | 9.4.1   | ✗      | 55304.8    | 17.58        | 9.86          |
| server-base-router       | 7.1.32  | ✓      | 54559.2    | 17.83        | 9.73          |
| connect                  | 3.7.0   | ✗      | 54224.8    | 17.95        | 9.67          |
| server-base              | 7.1.32  | ✗      | 53961.6    | 18.04        | 9.62          |
| yeps                     | 1.1.1   | ✗      | 51222.4    | 19.02        | 9.13          |
| micro-route              | 2.5.0   | ✓      | 49351.2    | 19.76        | 8.80          |
| connect-router           | 1.3.8   | ✓      | 48836.0    | 19.98        | 8.71          |
| trek-engine              | 1.0.5   | ✗      | 48083.2    | 20.30        | 7.89          |
| trek-router              | 1.2.0   | ✓      | 47278.4    | 20.65        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 45638.4    | 21.41        | 7.49          |
| yeps-router              | 1.2.0   | ✓      | 43735.2    | 22.37        | 7.80          |
| koa                      | 2.15.0  | ✗      | 42928.0    | 22.80        | 7.66          |
| spirit                   | 0.6.1   | ✗      | 41212.8    | 23.76        | 7.35          |
| spirit-router            | 0.5.0   | ✓      | 40649.6    | 24.12        | 7.25          |
| restify                  | 8.6.1   | ✓      | 39708.6    | 24.68        | 7.16          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 38820.6    | 25.26        | 6.92          |
| take-five                | 2.0.0   | ✓      | 38223.4    | 25.66        | 13.74         |
| total.js                 | 3.4.13  | ✓      | 38177.4    | 25.70        | 11.69         |
| koa-router               | 12.0.1  | ✓      | 37787.4    | 25.96        | 6.74          |
| hapi                     | 20.3.0  | ✓      | 33420.8    | 29.42        | 5.96          |
| microrouter              | 3.1.3   | ✓      | 32052.2    | 30.69        | 5.72          |
| trpc-router              | 9.27.4  | ✓      | 26476.4    | 37.27        | 5.86          |
| egg.js                   | 3.18.0  | ✓      | 17462.3    | 56.75        | 6.24          |
| express                  | 4.18.2  | ✓      | 13421.4    | 73.96        | 2.39          |
| fastify-big-json         | 4.25.2  | ✓      | 12631.2    | 78.62        | 145.33        |
| express-with-middlewares | 4.18.2  | ✓      | 12243.0    | 81.13        | 4.55          |
| express-route-prefix     | 4.18.2  | ✓      | 10735.6    | 92.56        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

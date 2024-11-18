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
* __Run:__ Mon Nov 18 2024 02:46:08 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68278.0    | 14.14        | 12.18         |
| polkadot                 | 1.0.0   | ✗      | 68147.2    | 14.18        | 12.15         |
| h3                       | 0.8.6   | ✗      | 64230.0    | 15.08        | 10.53         |
| h3-router                | 0.8.6   | ✓      | 63374.8    | 15.28        | 10.40         |
| bare                     | 10.13.0 | ✗      | 60117.6    | 16.13        | 10.72         |
| foxify                   | 0.10.20 | ✓      | 60006.4    | 16.16        | 9.84          |
| restana                  | 4.9.9   | ✓      | 58834.4    | 16.47        | 10.49         |
| polka                    | 0.5.2   | ✓      | 57924.0    | 16.76        | 10.33         |
| connect                  | 3.7.0   | ✗      | 57547.2    | 16.89        | 10.26         |
| fastify                  | 4.28.1  | ✓      | 55384.0    | 17.56        | 9.93          |
| micro                    | 9.4.1   | ✗      | 54248.8    | 17.93        | 9.67          |
| server-base-router       | 7.1.32  | ✓      | 53192.0    | 18.30        | 9.49          |
| yeps                     | 1.1.1   | ✗      | 52775.2    | 18.45        | 9.41          |
| server-base              | 7.1.32  | ✗      | 52309.6    | 18.62        | 9.33          |
| connect-router           | 1.3.8   | ✓      | 50208.8    | 19.42        | 8.95          |
| micro-route              | 2.5.0   | ✓      | 49417.6    | 19.73        | 8.81          |
| trek-engine              | 1.0.5   | ✗      | 48080.8    | 20.30        | 7.89          |
| trek-router              | 1.2.0   | ✓      | 47728.8    | 20.46        | 7.83          |
| vapr                     | 0.6.0   | ✓      | 46135.2    | 21.18        | 7.57          |
| yeps-router              | 1.2.0   | ✓      | 43589.6    | 22.44        | 7.77          |
| spirit                   | 0.6.1   | ✗      | 43259.2    | 22.60        | 7.71          |
| spirit-router            | 0.5.0   | ✓      | 42616.0    | 22.97        | 7.60          |
| koa                      | 2.15.3  | ✗      | 42436.0    | 23.07        | 7.57          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39661.4    | 24.71        | 7.07          |
| restify                  | 8.6.1   | ✓      | 38965.4    | 25.15        | 7.02          |
| total.js                 | 3.4.13  | ✓      | 38900.8    | 25.21        | 11.91         |
| take-five                | 2.0.0   | ✓      | 38233.0    | 25.66        | 13.75         |
| koa-router               | 12.0.1  | ✓      | 36226.2    | 27.10        | 6.46          |
| hapi                     | 20.3.0  | ✓      | 32277.0    | 30.48        | 5.76          |
| microrouter              | 3.1.3   | ✓      | 31769.0    | 30.97        | 5.67          |
| trpc-router              | 9.27.4  | ✓      | 26300.4    | 37.51        | 5.82          |
| egg.js                   | 3.28.0  | ✓      | 17545.7    | 56.48        | 6.27          |
| express                  | 4.21.1  | ✓      | 13737.8    | 72.26        | 2.45          |
| fastify-big-json         | 4.28.1  | ✓      | 12956.2    | 76.62        | 149.05        |
| express-with-middlewares | 4.21.1  | ✓      | 12518.0    | 79.33        | 4.66          |
| express-route-prefix     | 4.21.1  | ✓      | 10905.6    | 91.11        | 4.03          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

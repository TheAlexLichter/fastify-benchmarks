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
* __Run:__ Mon Oct 14 2024 02:40:34 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 70043.6    | 13.79        | 12.49         |
| polkadot                 | 1.0.0   | ✗      | 67072.4    | 14.43        | 11.96         |
| h3                       | 0.8.6   | ✗      | 61957.6    | 15.63        | 10.16         |
| h3-router                | 0.8.6   | ✓      | 60983.2    | 15.91        | 10.00         |
| restana                  | 4.9.9   | ✓      | 60940.8    | 15.92        | 10.87         |
| bare                     | 10.13.0 | ✗      | 59784.8    | 16.23        | 10.66         |
| polka                    | 0.5.2   | ✓      | 58163.2    | 16.70        | 10.37         |
| foxify                   | 0.10.20 | ✓      | 57389.6    | 16.93        | 9.41          |
| connect                  | 3.7.0   | ✗      | 57131.2    | 17.01        | 10.19         |
| fastify                  | 4.28.1  | ✓      | 56185.6    | 17.30        | 10.07         |
| micro                    | 9.4.1   | ✗      | 55223.2    | 17.61        | 9.85          |
| server-base              | 7.1.32  | ✗      | 54403.2    | 17.88        | 9.70          |
| server-base-router       | 7.1.32  | ✓      | 54020.8    | 18.01        | 9.63          |
| yeps                     | 1.1.1   | ✗      | 52124.8    | 18.69        | 9.30          |
| connect-router           | 1.3.8   | ✓      | 50483.2    | 19.31        | 9.00          |
| micro-route              | 2.5.0   | ✓      | 49792.8    | 19.58        | 8.88          |
| trek-engine              | 1.0.5   | ✗      | 48307.2    | 20.20        | 7.92          |
| trek-router              | 1.2.0   | ✓      | 47295.2    | 20.65        | 7.76          |
| vapr                     | 0.6.0   | ✓      | 45366.4    | 21.55        | 7.44          |
| spirit                   | 0.6.1   | ✗      | 44046.4    | 22.23        | 7.85          |
| yeps-router              | 1.2.0   | ✓      | 43590.4    | 22.44        | 7.77          |
| spirit-router            | 0.5.0   | ✓      | 43090.4    | 22.70        | 7.68          |
| koa                      | 2.15.3  | ✗      | 42591.2    | 22.99        | 7.60          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 40075.8    | 24.45        | 7.15          |
| total.js                 | 3.4.13  | ✓      | 39589.8    | 24.76        | 12.12         |
| restify                  | 8.6.1   | ✓      | 39409.6    | 24.87        | 7.10          |
| take-five                | 2.0.0   | ✓      | 38820.6    | 25.26        | 13.96         |
| koa-router               | 12.0.1  | ✓      | 37427.0    | 26.22        | 6.67          |
| hapi                     | 20.3.0  | ✓      | 33853.2    | 29.03        | 6.04          |
| microrouter              | 3.1.3   | ✓      | 32158.4    | 30.59        | 5.73          |
| trpc-router              | 9.27.4  | ✓      | 26252.4    | 37.59        | 5.81          |
| egg.js                   | 3.28.0  | ✓      | 17393.0    | 56.96        | 6.22          |
| express                  | 4.21.1  | ✓      | 13781.8    | 72.03        | 2.46          |
| fastify-big-json         | 4.28.1  | ✓      | 12938.2    | 76.76        | 148.86        |
| express-with-middlewares | 4.21.1  | ✓      | 12475.2    | 79.61        | 4.64          |
| express-route-prefix     | 4.21.1  | ✓      | 10831.2    | 91.74        | 4.01          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

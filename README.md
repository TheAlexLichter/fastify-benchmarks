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
* __Node:__ `v14.21.2`
* __Run:__ Mon Jan 30 2023 02:29:50 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| bare                     | 10.13.0 | ✗      | 51827.2    | 18.81        | 9.24          |
| foxify                   | 0.10.20 | ✓      | 50816.0    | 19.18        | 8.34          |
| connect                  | 3.7.0   | ✗      | 50747.2    | 19.21        | 9.05          |
| polkadot                 | 1.0.0   | ✗      | 50676.0    | 19.24        | 9.04          |
| polka                    | 0.5.2   | ✓      | 50156.0    | 19.44        | 8.94          |
| h3                       | 0.8.6   | ✗      | 49110.4    | 19.87        | 8.05          |
| h3-router                | 0.8.6   | ✓      | 49015.2    | 19.91        | 8.04          |
| micro                    | 9.4.1   | ✗      | 48993.6    | 19.91        | 8.74          |
| server-base              | 7.1.32  | ✗      | 48655.2    | 20.06        | 8.68          |
| 0http                    | 3.4.2   | ✓      | 48015.2    | 20.33        | 8.56          |
| server-base-router       | 7.1.32  | ✓      | 47870.4    | 20.39        | 8.54          |
| connect-router           | 1.3.7   | ✓      | 46212.0    | 21.15        | 8.24          |
| yeps                     | 1.1.1   | ✗      | 45484.0    | 21.49        | 8.11          |
| micro-route              | 2.5.0   | ✓      | 45412.2    | 21.53        | 8.10          |
| restana                  | 4.9.7   | ✓      | 45106.4    | 21.68        | 8.04          |
| trek-router              | 1.2.0   | ✓      | 41946.6    | 23.34        | 6.88          |
| trek-engine              | 1.0.5   | ✗      | 41319.8    | 23.71        | 6.78          |
| vapr                     | 0.6.0   | ✓      | 41245.8    | 23.75        | 6.77          |
| yeps-router              | 1.2.0   | ✓      | 38539.4    | 25.46        | 6.87          |
| spirit                   | 0.6.1   | ✗      | 37728.2    | 26.03        | 6.73          |
| spirit-router            | 0.5.0   | ✓      | 36283.8    | 27.07        | 6.47          |
| fastify                  | 4.12.0  | ✓      | 35723.8    | 27.49        | 6.40          |
| koa                      | 2.14.1  | ✗      | 35589.0    | 27.60        | 6.35          |
| koa-isomorphic-router    | 1.0.1   | ✓      | 34804.6    | 28.24        | 6.21          |
| take-five                | 2.0.0   | ✓      | 34451.4    | 28.53        | 12.39         |
| total.js                 | 3.4.13  | ✓      | 34069.0    | 28.85        | 10.43         |
| restify                  | 8.6.1   | ✓      | 32134.2    | 30.61        | 5.79          |
| koa-router               | 12.0.0  | ✓      | 31779.6    | 30.97        | 5.67          |
| hapi                     | 20.2.2  | ✓      | 27494.0    | 35.86        | 4.90          |
| microrouter              | 3.1.3   | ✓      | 26310.0    | 37.50        | 4.69          |
| trpc-router              | 9.27.3  | ✓      | 20006.4    | 49.46        | 4.43          |
| egg.js                   | 3.15.0  | ✓      | 13059.6    | 76.03        | 4.67          |
| express                  | 4.18.2  | ✓      | 10914.3    | 91.04        | 1.95          |
| express-with-middlewares | 4.18.2  | ✓      | 9419.5     | 105.54       | 3.50          |
| express-route-prefix     | 4.18.2  | ✓      | 9252.0     | 107.50       | 3.42          |
| fastify-big-json         | 4.12.0  | ✓      | 9208.5     | 108.22       | 105.95        |
| rayo                     | 1.4.0   | ✓      | N/A        | N/A          | N/A           |

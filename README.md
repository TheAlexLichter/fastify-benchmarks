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
* __Run:__ Mon Mar 30 2026 04:19:45 GMT+0000 (Coordinated Universal Time)
* __Method:__ `autocannon -c 100 -d 40 -p 10 localhost:3000` (two rounds; one to warm-up, one to measure)

|                          | Version | Router | Requests/s | Latency (ms) | Throughput/Mb |
| :--                      | --:     | --:    | :-:        | --:          | --:           |
| 0http                    | 3.5.3   | ✓      | 68603.2    | 14.07        | 12.23         |
| polkadot                 | 1.0.0   | ✗      | 67480.0    | 14.33        | 12.03         |
| h3                       | 0.8.6   | ✗      | 63268.0    | 15.31        | 10.38         |
| restana                  | 4.9.9   | ✓      | 62626.4    | 15.46        | 11.17         |
| h3-router                | 0.8.6   | ✓      | 61863.2    | 15.68        | 10.15         |
| bare                     | 10.13.0 | ✗      | 61654.4    | 15.72        | 10.99         |
| polka                    | 0.5.2   | ✓      | 60152.0    | 16.13        | 10.73         |
| foxify                   | 0.10.20 | ✓      | 59192.8    | 16.40        | 9.71          |
| micro                    | 9.4.1   | ✗      | 58301.6    | 16.66        | 10.40         |
| server-base              | 7.1.32  | ✗      | 57546.4    | 16.87        | 10.26         |
| connect                  | 3.7.0   | ✗      | 57387.2    | 16.92        | 10.23         |
| fastify                  | 4.29.1  | ✓      | 56702.4    | 17.13        | 10.17         |
| server-base-router       | 7.1.32  | ✓      | 54844.0    | 17.74        | 9.78          |
| connect-router           | 1.3.8   | ✓      | 51906.4    | 18.77        | 9.26          |
| yeps                     | 1.1.1   | ✗      | 51650.4    | 18.86        | 9.21          |
| micro-route              | 2.5.0   | ✓      | 50122.4    | 19.46        | 8.94          |
| trek-engine              | 1.0.5   | ✗      | 48106.4    | 20.29        | 7.89          |
| trek-router              | 1.2.0   | ✓      | 48084.8    | 20.30        | 7.89          |
| vapr                     | 0.6.0   | ✓      | 46001.6    | 21.24        | 7.55          |
| yeps-router              | 1.2.0   | ✓      | 43768.0    | 22.35        | 7.80          |
| koa                      | 2.16.4  | ✗      | 43196.8    | 22.64        | 7.70          |
| spirit                   | 0.6.1   | ✗      | 41084.0    | 23.84        | 7.33          |
| spirit-router            | 0.5.0   | ✓      | 40896.8    | 23.96        | 7.29          |
| take-five                | 2.0.0   | ✓      | 39851.8    | 24.60        | 14.33         |
| total.js                 | 3.4.13  | ✓      | 39826.4    | 24.61        | 12.19         |
| koa-isomorphic-router    | 1.0.1   | ✓      | 39613.4    | 24.74        | 7.06          |
| restify                  | 8.6.1   | ✓      | 39341.4    | 24.91        | 7.09          |
| koa-router               | 12.0.1  | ✓      | 36967.0    | 26.55        | 6.59          |
| hapi                     | 20.3.0  | ✓      | 33035.8    | 29.76        | 5.89          |
| microrouter              | 3.1.3   | ✓      | 32345.6    | 30.41        | 5.77          |
| trpc-router              | 9.27.4  | ✓      | 27024.0    | 36.50        | 5.98          |
| egg.js                   | 3.34.0  | ✓      | 17814.0    | 55.58        | 6.37          |
| express                  | 4.22.1  | ✓      | 13434.6    | 73.90        | 2.40          |
| express-with-middlewares | 4.22.1  | ✓      | 12359.0    | 80.34        | 4.60          |
| fastify-big-json         | 4.29.1  | ✓      | 12253.4    | 81.05        | 140.98        |
| express-route-prefix     | 4.22.1  | ✓      | 10735.4    | 92.58        | 3.97          |
| rayo                     | 1.4.6   | ✓      | N/A        | N/A          | N/A           |

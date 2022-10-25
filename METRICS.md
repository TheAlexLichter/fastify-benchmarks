# Metrics
* __Machine:__ linux x64 | 2 vCPUs | 6.8GB Mem
* __Node:__ `v14.20.1`
* __Run:__ Tue Oct 25 2022 10:47:28 GMT+0000 (Coordinated Universal Time)
* __Method:__ `npm run metrics` (samples: 5)
* __startup:__ time elapsed to setup the application
* __listen:__ time elapsed until the http server is ready to accept requests (cold start)

| | startup(ms) | listen(ms) |
|-| -       | -      |
| 1-startup-routes-schema.js | 125.34 | 179.72 |
| 1-startup-routes.js | 124.73 | 136.72 |
| 10-startup-routes-schema.js | 127.37 | 192.84 |
| 10-startup-routes.js | 126.76 | 140.73 |
| 100-startup-routes-schema.js | 142.84 | 330.67 |
| 100-startup-routes.js | 142.95 | 172.70 |
| 1000-startup-routes-schema.js | 331.99 | 1435.21 |
| 1000-startup-routes.js | 315.14 | 479.43 |
| 10000-startup-routes-schema.js | 4745.89 | 16382.67 |
| 10000-startup-routes.js | 4012.71 | 6953.58 |
| startup-listen.js | 124.08 | 136.73 |

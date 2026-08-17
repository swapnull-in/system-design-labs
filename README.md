# System Design Labs — the hub

The start-here page for a family of **ten hands-on TypeScript repos**, one per
Staff-level system-design topic. Every concept in every repo is:

1. a **runnable phase** (`npm run phaseN` — deterministic, dependency-free,
   heavily commented, ending in a takeaway),
2. a **live panel** in that repo's interactive web lab,
3. a **drill card** (the study path's real interview questions, click-to-reveal),
4. a row in that repo's `STUDY-GUIDE.md` mapping it to the study-module section.

## The family (study order)

| # | Repo | Lab |
|---|---|---|
| 01 | [messaging-queues](https://github.com/swapnull-in/messaging-queues) | Queue Lab |
| 02 | [databases](https://github.com/swapnull-in/databases) | Storage Lab |
| 03 | [caching](https://github.com/swapnull-in/caching) | Cache Lab |
| 04 | [realtime-delivery](https://github.com/swapnull-in/realtime-delivery) | Realtime Lab |
| 05 | [search-and-ranking](https://github.com/swapnull-in/search-and-ranking) | Search Lab |
| 06 | [blob-storage-cdn](https://github.com/swapnull-in/blob-storage-cdn) | Blob Lab |
| 07 | [stream-processing](https://github.com/swapnull-in/stream-processing) | Stream Lab |
| 08 | [geospatial](https://github.com/swapnull-in/geospatial) | Geo Lab |
| 09 | [rate-limiting](https://github.com/swapnull-in/rate-limiting) | Rate Lab |
| 10 | [distributed-systems](https://github.com/swapnull-in/distributed-systems) | Failure Lab |

## This repo

`web/index.html` is the hub page — serve it with `npm run web`, deploy with
`npm run deploy` (Cloudflare Pages, project `system-design-labs`), or connect
the repo in the Cloudflare dashboard with build output `web`.

MIT.

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

## Companion repo

[kafka-chat-pipeline](https://github.com/swapnull-in/kafka-chat-pipeline) is a
separate hands-on track rather than an eleventh lab: a chat pipeline on a real
Kafka broker with producers, consumer groups, offsets and the outbox pattern.
It has no web lab or drill cards and needs Kafka and Postgres running. Do it
after `messaging-queues`.

## This repo

The hub page and the build that publishes the whole family as **one site**:
the hub at `/`, each lab at `/<repo>/` (for example `/caching/`).

```bash
npm run build    # assemble dist/ from web/ plus every lab's web/
npm run web      # build, then serve dist/ at http://localhost:8080
npm run deploy   # build, then deploy dist/ to Cloudflare Pages (project `system-design-labs`)
```

The build takes each lab from a sibling checkout (`../caching`, …) when one
exists and otherwise clones it from GitHub; `LABS_REMOTE=1 npm run build`
always clones. To deploy from the Cloudflare dashboard instead, connect this
repo with build command `npm run build` and build output `dist`.

Serving everything from one origin means the labs don't each need their own
`<repo>.pages.dev` name, and the hub can read every lab's progress directly.

MIT.

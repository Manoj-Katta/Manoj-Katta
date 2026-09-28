<h1 align="center">Hi, I'm Manoj</h1>
<h3 align="center">
Software Engineer @ BrowserStack · Percy Platform · Backend & Platform Engineering
</h3>

---

### About Me

Software Engineer on the **Percy Platform team at BrowserStack**, working on the
infrastructure behind cross-browser visual testing: the pipeline that renders
customer DOM snapshots in real browsers, diffs them, and stores the results.

My work spans storage and data lifecycle on GCS, the Sidekiq/Redis job pipeline,
browser rendering infrastructure, and production debugging across a Rails API,
a Go proxy and a Node.js CLI. Previously interned at **Paytm** (payouts backend,
₹130cr/day) and did research on **C2PA / deepfake detection** at City, University of London.

---

### Things I've Shipped

**BrowserStack — Percy Platform**

- **GCS storage cost reduction** — built Percy's 3-month resource-retention deletion
  pipeline and a backlog sweep across ~1B+ eligible resources (120M+ deleted in
  production so far, 0 incorrect deletions in audited samples); separately verified
  no read path depends on orphaned object versions and rolled out a lifecycle rule
  targeting ~220 TB of them (82 TB reclaimed in the first phase).
  Projected savings: ~$25–34K/yr + ~$69K/yr.
- **Browser upgrades across the rendering stack** — shipped Firefox 146, Edge 142/143
  and Chrome 143 through base image, renderer, API, cache worker and CLI, with prod
  build replays for the go/no-go; isolated an Edge 143 render-latency regression to
  specific bundled browser features and disabled them.
- **Browser force-upgrade admin API** — replaced a prod-console procedure with a
  superuser API: dry-run preview, async runs, validation, rate limiting and
  single-flight locking, so any engineer can run or revert an upgrade safely.
- **Canary deploys for the job dispatcher** — threaded a canary flag from the API
  through Redis Lua into a pool-aware scheduler, with an isolated canary worker pool
  and a global kill switch. This closed the last uncovered component in the render
  pipeline's canary coverage.
- **[@percy/cli](https://www.npmjs.com/package/@percy/cli)** (500K+ weekly downloads) —
  [added popover and dialog capture](https://github.com/percy/cli/pull/2141) via
  `pseudoClassEnabledElements`, unblocking an enterprise deal.

**Paytm — Payouts backend (intern)**

- **Merchant payouts** — worked on the backend behind ₹130+ crore in daily merchant
  payouts: commission workflows, reporting modules for revenue reconciliation, and
  hardened error handling in transaction flows.
- **Report automation** — set up a RabbitMQ staging cluster to automate report
  generation, removing manual steps; fixed an Elasticsearch fetch error that was
  blocking report generation.
- **Gold Coin launch** — built the payout-side changes for the Gold team's new
  Gold Coin feature.

---

### Tech Stack

**Languages:** Ruby · JavaScript / Node.js · Go · Java

**Backend:** Rails · Sidekiq · Express · REST APIs

**Cloud / Infra:** GCP (GCS, Cloud Monitoring) · Kubernetes · Docker · Helm · Terraform · CI/CD

**Data:** MySQL · Redis · MongoDB · BigQuery · Elasticsearch

**Messaging:** Kafka · RabbitMQ

**Observability:** Honeycomb · Datadog · LaunchDarkly (feature flags)

---

### Currently

- Draining a ~1B-resource deletion backlog on a shared worker fleet without starving the steady-state lane
- Building a RAG application in public — [rag_application](https://github.com/Manoj-Katta/rag_application)

---

📫 manojkatta1173@gmail.com · [LinkedIn](https://linkedin.com/in/manoj-katta-209a00228) · [Portfolio](https://manoj-katta-portfolio.netlify.app/)

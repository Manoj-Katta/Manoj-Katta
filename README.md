<h1 align="center">Hi, I'm Manoj</h1>
<h3 align="center">
Software Engineer @ BrowserStack · Percy · Backend & Platform Engineering
</h3>

---

### About Me

Software Engineer on the **Percy team at BrowserStack**, working across backend
features and the platform behind cross-browser visual testing: the system that
captures customer DOM snapshots, renders them in real browsers, diffs them, and
stores the results.

I ship product features in the Rails API and the Node.js CLI and SDKs, and I work on
the platform underneath them: storage and data lifecycle on GCS, the Sidekiq/Redis
job pipeline, and browser rendering infrastructure. Previously interned at **Paytm**
(payouts backend handling ₹130cr/day) and did research on **C2PA / deepfake detection** at
City, University of London.

---

### Things I've Shipped

**BrowserStack — Percy**

- **Popover and dialog capture in [@percy/cli](https://www.npmjs.com/package/@percy/cli)**
  (500K+ weekly downloads) — [extended selective pseudo-class capture](https://github.com/percy/cli/pull/2141)
  to popover and dialog elements and added SDK global config, unblocking an enterprise deal.
- **Resource-retention deletion pipeline** — designed and built the pipeline that deletes
  page-asset resources 3 months after last use, plus a backlog sweep on a shared worker
  fleet across ~1B+ eligible resources, with a touch guard so assets a live build still
  uses are never deleted. Targets ~$25–34K/yr in GCS savings.
- **Browser upgrades across the rendering stack** — shipped Firefox 146, Edge 142/143
  and Chrome 143 through base image, renderer, API, cache worker and CLI, with prod
  build replays for the go/no-go. Traced an Edge render-latency regression to its
  bundled AI features (Copilot, on-device Phi-4-mini, Web AI APIs) and disabled them in
  Edge 142 and 143, cutting the added per-snapshot latency from ~2s to under 500ms;
  benchmarked both and shipped Edge 142 as the faster build.
- **Browser force-upgrade admin API** — replaced a prod-console procedure with a
  superuser API: dry-run preview, async runs, validation, rate limiting and
  single-flight locking, so any engineer can run or revert an upgrade safely.
- **Canary deploys for the job dispatcher** — threaded a canary flag from the API
  through Redis Lua into a pool-aware scheduler, with an isolated canary worker pool
  and a global kill switch. This closed the last uncovered component in the render
  pipeline's canary coverage.

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

**Languages:** Ruby · JavaScript / Node.js · Java

**Backend:** Rails · Sidekiq · Express · REST APIs

**Cloud / Infra:** GCP (GCS, Cloud Monitoring) · Kubernetes · Docker · Helm · Terraform · CI/CD

**Data:** MySQL · Redis · MongoDB · BigQuery · Elasticsearch

**Messaging:** Kafka · RabbitMQ

**Observability:** Honeycomb · Datadog · LaunchDarkly (feature flags)

---

📫 manojkatta1173@gmail.com · [LinkedIn](https://linkedin.com/in/manoj-katta-209a00228)

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

- **Popover capture in [@percy/cli](https://www.npmjs.com/package/@percy/cli)**
  (500K+ weekly downloads) — [built popover capture](https://github.com/percy/cli/pull/2141)
  across the CLI (v1.31.11), the render cache worker and the Ember SDK (v5.0.1),
  unblocking an enterprise deal.
- **Resource-retention deletion pipeline** — designed the pipeline over ~1B+ eligible
  page assets, on its own worker pods and queues, with a guard so assets a live build
  still uses are never deleted. It has removed ~45 TB from the resources bucket so far,
  cutting ~$14K a year in ongoing storage cost, and keeps deleting as assets age out.
- **Browser upgrades, end to end** — own Percy's desktop browser upgrades across base
  image, renderer, API, cache worker and CLI. Traced an Edge render-latency regression
  to bundled AI features and cut the added per-snapshot latency from ~2s to under
  500ms; built an admin API with dry-run preview that replaced a production-console
  upgrade procedure.
- **Canary deploys for the job dispatcher** — threaded a canary flag from the API
  through Redis Lua into a pool-aware scheduler, with an isolated canary worker pool
  and a global kill switch.
- **On-call noise** — reworked the Sidekiq, compare-job and rendering-proxy alerts
  (about 95% less page noise on the proxy alert), and replaced ~6.2M per-terminal
  health-check pager events a week with one summary per pool.

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

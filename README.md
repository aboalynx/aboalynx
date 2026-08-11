<picture>
  <source media="(prefers-color-scheme: dark)" srcset="brand/Aboalynx_Logo_Inverted.svg">
  <img alt="Aboalynx" src="brand/Aboalynx_Logo_Primary.svg" width="420">
</picture>

### Backend engineer — PHP/Laravel and Node.js/NestJS

I build the parts of a product that have to stay correct under load: multi-tenant
architecture, payment integrations, booking systems where two people click the same
thing at the same millisecond, and event pipelines that keep working when traffic
spikes. Ten years of it, most recently as technical lead on a multi-tenant SaaS
platform.

Based in Egypt, working remotely.

---

## Featured

### [@aboalynx/payment](https://github.com/aboalynx/payment)

[![npm](https://img.shields.io/npm/v/@aboalynx/payment)](https://www.npmjs.com/package/@aboalynx/payment)
[![CI](https://github.com/aboalynx/payment/actions/workflows/ci.yml/badge.svg)](https://github.com/aboalynx/payment/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/aboalynx/payment/blob/main/LICENSE)

Gateway-agnostic payment processing for NestJS. One interface over Stripe and PayPal, so
changing provider is a configuration change rather than a code change.

Capability interfaces and discriminated-union results make the compiler force callers to
handle every payment outcome, not just the happy path. A shared contract suite runs the
same assertions against every gateway — which is how I found that `capture()` meant two
different things on the two providers, and fixed it.

128 tests · 97% statement coverage · CI on Node 20 and 22 · published from CI with build
provenance.

```sh
npm i @aboalynx/payment
```

### [seatmap](https://github.com/aboalynx/seatmap)

A NestJS service answering one question properly: what happens when thousands of people
click the same seat at the same millisecond?

Redis holds seats optimistically with a TTL, PostgreSQL decides what has actually been
sold, and the test suite fires 200 simultaneous requests at a single seat and asserts
that exactly one of them wins.

Write-up: [What happens when 20,000 people click the same seat?](https://dev.to/aboalynx/what-happens-when-20000-people-click-the-same-seat-245n)

---

## What I've built

**Multi-tenant SaaS for charity and education organisations.** Laravel Octane on
FrankenPHP with a Next.js BFF frontend, database-per-tenant isolation, and a hybrid
provisioning model that lets certain tenants keep their database on their own servers —
custom bootstrapper, scoped credential management, auto-provisioning with rollback.

**Stadium ticketing and attendance.** Seat booking driven entirely by SVG venue maps,
handling 12,000–20,000 spectators per fixture, with admin-side seat distribution wired
to ticket types.

**Behavioural analytics pipeline.** Browser SDK → signed edge relay → write-key
verification → RabbitMQ → ClickHouse, feeding a high-volume dashboard. I designed the
flow and built the backend and relay.

---

## Stack

- **Backend** — PHP, Laravel, Laravel Octane, FrankenPHP, Horizon, Node.js, NestJS, TypeScript
- **Data** — PostgreSQL, MySQL, ClickHouse, Redis, RabbitMQ
- **Frontend** — Next.js, Vue, Flutter
- **Infra** — Docker, Debian, PgBouncer, Prometheus, Sentry
- **AI** — RAG pipelines, vector databases, local LLMs (Ollama), spec-driven development workflows

---

## Reach me

Open to remote backend roles.

- Writing at [dev.to/aboalynx](https://dev.to/aboalynx)
- LinkedIn — [linkedin.com/in/mohamedabdelbary1985](https://www.linkedin.com/in/mohamedabdelbary1985)
- Email — [m.abdelbary.a@gmail.com]

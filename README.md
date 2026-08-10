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

### What I've built

**Multi-tenant SaaS for charity and education organisations.** Laravel Octane on
FrankenPHP with a Next.js BFF frontend, database-per-tenant isolation, and a hybrid
provisioning model that lets certain tenants keep their database on their own
servers — custom bootstrapper, scoped credential management, auto-provisioning with
rollback. Also built the payment layer: one package, one call signature, several
providers behind it.

**Stadium ticketing and attendance.** Seat booking driven entirely by SVG venue maps,
handling 12,000–20,000 spectators per fixture, with admin-side seat distribution wired
to ticket types.

**Behavioural analytics pipeline.** Browser SDK → signed edge relay → write-key
verification → RabbitMQ → ClickHouse, feeding a high-volume dashboard. I designed the
flow and built the backend and relay.

---

### Stack

**Backend** · PHP, Laravel, Laravel Octane, FrankenPHP, Horizon, Node.js, NestJS, TypeScript
**Data** · PostgreSQL, MySQL, ClickHouse, Redis, RabbitMQ
**Frontend** · Next.js, Vue, Flutter
**Infra** · Docker, Debian, PgBouncer, Prometheus, Sentry
**AI** · RAG pipelines, vector databases, local LLMs (Ollama), spec-driven development workflows

---

### Featured

**[seatmap](https://github.com/aboalynx/seatmap)** — a NestJS service answering one
question properly: what happens when thousands of people click the same seat at once.
Redis holds seats optimistically with a TTL, PostgreSQL decides what was actually sold,
and the test suite fires 200 simultaneous requests at a single seat to prove exactly
one wins.

---

### Reach me

- Email — m.abdelbary.a@gmail.com
- LinkedIn — https://www.linkedin.com/in/mohamedabdelbary1985
- Open to remote backend roles

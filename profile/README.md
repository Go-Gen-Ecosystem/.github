# Go-Gen Ecosystem

A modular Go development toolkit: focused, standalone modules that work together.

| Module | Purpose |
|---|---|
| [halolog](https://github.com/go-gen-ecosystem/halolog) | Zero-allocation structured logging — 0 allocs/op on the hot path, guarded by committed tests; ships `halologgen`, a schema-to-facade generator with byte-diff-verified determinism |
| go-migrate | Database migrations: Go-native, single-binary Flyway alternative — CLI and embeddable library |
| go-gen-observer | Observability: Prometheus metrics, OpenTelemetry tracing, health checks |
| go-gen-resilience | Resilience patterns: circuit breaker, retry, timeout, bulkhead, rate limiting, caching |
| go-gen-security | Security primitives: encryption, hashing, signing, sanitization, CORS |
| go-gen-framework | Runtime libraries: auth, config, messaging, logging, lifecycle runner |
| go-gen | Code generator CLI — project scaffolding and CRUD module generation |

Unlinked modules are being published in sequence — each lands only after passing
the gate below.

## How this organization ships

- **Standalone first** — every module is independently useful. Use one, some, or
  all; nothing drags in an umbrella framework.
- **Zero lock-in** — plain Go, plain interfaces, Apache-2.0. Adopting a module
  never commits you to a platform or to the rest of this organization.
- **Every claim reproducible** — performance numbers ship with the exact
  benchmark commands, hardware notes, and methodology that produced them.
- **Deterministic tooling** — code generators are pinned by committed
  regeneration tests: same input, byte-identical output, every time.
- **Published only past the gate** — cross-platform builds, race-clean tests,
  uncapped lint at zero issues, vulnerability scanning, and a claims-audited
  README, before anything gets a public repo or a version tag.

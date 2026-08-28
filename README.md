# go-gen-ecosystem/.github

Org-wide defaults and shared CI for the Go-Gen Ecosystem.

- `.github/workflows/reusable-go-ci.yml` — reusable CI (lint, build, test with race + coverage gate, ubuntu + windows matrix). Called from every module repo.
- `profile/README.md` — organization profile page.
- `templates/` — files stamped into each module repo:
  - `.golangci.yml` — shared lint config (golangci-lint v2; enforces interface size ≤ 6 and no fmt printing in shipped packages)
  - `.gitignore` — shared ignore rules
  - `ci.yml`, `release.yml` — per-repo workflow callers
  - `.goreleaser-lib.yml`, `.goreleaser-cli.yml` — release configs for libraries vs CLIs
  - `pre-push` — local git gate (`git config core.hooksPath .githooks`)

@author Admilson B. F. Cossa

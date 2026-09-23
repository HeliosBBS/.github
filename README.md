# HeliosBBS/.github

Estate-wide defaults for every repository in the organisation. GitHub serves the community
health files here to any repository that does not carry its own copy; the workflows here are
called by each repository's thin CI, so a rule is written once.

| Path | What it is |
|---|---|
| `SECURITY.md`, `CONTRIBUTING.md` | inherited by every repository |
| `ISSUE_TEMPLATE/work-item.yml` | the issue form that enforces the work-order shape |
| `PULL_REQUEST_TEMPLATE.md` | the PR checklist |
| `labels.json` | the one label set; `sync-labels.yml` applies it to every repository |
| `.github/workflows/check.yml` | reusable: `make check` on Linux amd64, Linux arm64 and Windows |
| `.github/workflows/scorecard.yml` | reusable: OpenSSF Scorecard |
| `.github/workflows/release.yml` | reusable: build the three targets, attest provenance, attach an SBOM |
| `.github/workflows/add-to-project.yml` | reusable: put a new issue or PR on the estate board |
| `.github/workflows/estate.yml` | the estate scheduler |

Each repository's `CONSTITUTION.md` and the shared constitution in the `HeliosSkills` plugin are
the authority; nothing here restates them.

# opsforge-azure-cost-inventory

Azure cost and inventory reporting (read-only).

> **Status: not started — scaffold only.** This repository reserves the structure for the automation and records its intended scope. It contains no working code yet, and nothing here has been tested or run against any infrastructure.

Part of the [OpsForge](https://github.com/NPKpadala/opsforge-core) family. Reference implementation to copy the layout from: [opsforge-linux-health](https://github.com/NPKpadala/opsforge-linux-health).

## Planned scope

- Subscription resource inventory
- Cost breakdown by tag/resource group
- Scheduled CSV/HTML reports

## Design rules (shared by every OpsForge automation)

- Depends on a pinned `opsforge-core` release; plugin registered via the `opsforge.plugins` entry point.
- Real adapter boundary (Azure SDK / REST) that is mocked in CI; no static fake results.
- YAML configuration, `env:` credential references, secret redaction, JSON audit trail, retries, JSON reports.
- Read-only: no mutations, so no approval gate.

## Implementation matrix

| Area | Implemented | Tests | Dry-run | Reporting | Real-infra verified |
|---|---|---|---|---|---|
| Collection adapter | no | no | n/a | no | no |
| Evaluation | no | no | n/a | no | no |
| Reporting | no | no | n/a | no | no |
| Packaging / CI / Docker | no | no | n/a | n/a | no |

## License

MIT

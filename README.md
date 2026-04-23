# fleet-management-git-sync

Pipelines under `pipelines/` sync to [Grafana Fleet Management](https://github.com/grafana/fleet-management-sync-action) via GitHub Actions.

## Required repository secrets

| Secret | Description |
|--------|-------------|
| `FM_URL` | Fleet Management base API URL (for example `https://fleet-management-prod-001.grafana.net`) |
| `FM_USERNAME` | Fleet Management username |
| `FM_TOKEN` | Grafana Cloud API token with `fleet-management:write` |

Each pipeline needs a YAML metadata file and an Alloy file with the same base name in the same directory. The workflow namespace is the repository name so cleanup only affects pipelines from this repo’s Git source and that namespace.
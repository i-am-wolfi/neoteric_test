# neoteric_test

Repo descartável para testar build da Neoteric (marble) via GitHub Actions, sem Crave.

## Workflows

* `build-neoteric-marble-cnb.yml` — Android 17 (`manifest -b cnb` + `local_manifests/marble-cnb.xml` com branches `cnb` + fallback `bka-8450`)
* `build-neoteric-marble-bka.yml` — Android 16 (`manifest -b bka`, `marble.xml` já vem no manifest)

## Como rodar

1. Actions > escolhe o workflow > Run workflow.
2. Zip sai em Artifacts + Release (`marble-cnb-N` / `marble-bka-N`).
3. Primeiro build full pode bater o limite de 6h — roda de novo que o incremental com ccache continua.

## Depois

Pode apagar o repo: `gh repo delete i-am-wolfi/neoteric_test --yes`.

# Flutter App — Camillia workspace template

A Camillia Community Hub workspace template for teams building a Flutter app for
Android and iOS that ships on a fortnightly release train.

## What's inside

The `workspace/` directory is the template's `.workspace` contract tree:

```
workspace/
  README.md                     workspace overview and agent navigation guide
  rules/
    dart-flutter.md             null safety, widgets, lint rules
    app-architecture.md         Riverpod layering, navigation, networking
  conventions/
    naming.md                   files, widgets, providers, branches
    testing.md                  unit/widget/golden/integration testing
    release-train.md            cadence, code freeze, hotfixes, rollout
    commits.md                  conventional commits and PR rules
  repositories/
    app.md                      repo descriptor: layout, flutter commands
  business/
    glossary.md                 app domain vocabulary skeleton
    rules.md                    numbered business rules skeleton
  architecture/
    components.md               app and backend components
    decisions/README.md         ADR format and decision log
  technical/constraints/
    versions.md                 pinned Flutter/Dart/SDK versions
    stores.md                   store distribution and privacy constraints
  ui/
    map.md                      routes and screens map
```

Two payload areas have special meaning to the product rather than to the
workspace tree: `template.json` declares the expected repositories (see
[Template contract](#template-contract)), and `repos/` carries the seed
content the wizard applies to them (`app`).

## How to use

Install from the Camillia Community Hub, then create a workspace from this
template. Camillia installs the `workspace/` tree as the new workspace's
`.workspace` contract: the agent reads these rules, conventions, repository
descriptors and docs skeletons before every task. Where the workspace files
carry `{{ projectName }}` or `{{ orgName }}` tokens, they are substituted with
your project and organization names when the template is applied — no manual
placeholder hunt. After installation, replace the example domain (a ride app)
with your own, point the repository descriptor at your real repo and adjust
the pinned versions to your stack.

## Template contract

`template.json` declares the repositories this product is made of; the
workspace wizard walks each one and offers to **create** a fresh repo at your
git provider or **load** an existing one:

| Key | Label | Description | Required | Override default |
|---|---|---|---|---|
| `app` | Flutter app | Flutter application | yes | no |

Seed content for each repo lives under `repos/<key>/` (a starter README and
`.gitignore`). Applying a seed to a repo that already has content requires the
"authorize content override" choice in the wizard; before anything is
overwritten the current branch heads are tagged
`camillia-backup/template-<yyyyMMdd-HHmmss>`, so existing work is never lost.

Replacement tokens — `{{ orgName }}`, `{{ projectName }}` and `{{ projectId }}`
— are substituted across all workspace-bound files at apply time. See the
[extension guidelines](https://github.com/camillia-hub/extension-guidelines)
for the full template contract.

## License

MIT — see [LICENSE](LICENSE).

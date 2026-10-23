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

## How to use

Install from the Camillia Community Hub, then create a workspace from this
template. Camillia installs the `workspace/` tree as the new workspace's
`.workspace` contract: the agent reads these rules, conventions, repository
descriptors and docs skeletons before every task. After installation, replace the
example domain (a ride app) with your own, point the repository descriptor at
your real repo and adjust the pinned versions to your stack.

## License

MIT — see [LICENSE](LICENSE).

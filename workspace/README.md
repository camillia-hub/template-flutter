# App workspace: Flutter

This workspace builds **{{ projectName }}**, a Flutter application for Android and iOS that
ships on a fortnightly release train (see `repositories/app.md` and
`conventions/release-train.md`).

## How the agent should navigate this workspace

Read in this order before your first task:

1. `rules/` — mandatory rules: `dart-flutter.md` (language and widget rules) and
   `app-architecture.md` (Riverpod layering). Rules win over conventions when
   they conflict.
2. `conventions/` — naming, testing, the release train and commit style. The
   release train decides *when* work may merge, not just how.
3. `repositories/app.md` — the repository layout and every build/test command.
   Run the quick check listed there before you call a change done.
4. `business/` — the domain vocabulary (`glossary.md`) and numbered business
   rules (`rules.md`); use these exact terms in code and UI copy.
5. `architecture/components.md` and `architecture/decisions/` — the system shape
   and the ADR log; add an ADR when you change something structural.
6. `technical/constraints/` — pinned Flutter/Dart versions and the store rules.
7. `ui/map.md` — the app's route map; keep it in sync when routes change.

When a task teaches you a durable fact about the domain, record it in
`business/glossary.md` or `business/rules.md` — not only in the task paper.

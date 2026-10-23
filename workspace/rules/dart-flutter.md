# Dart and Flutter rules

Mandatory for every change in the `app` repository.

- Dart 3 with sound null safety; never force-unwrap with `!` unless a local null
  check proves safety, and never in production code paths without that proof.
- `flutter analyze` (with the workspace `analysis_options.yaml`, based on
  `flutter_lints`) must be warning-free; formatting is enforced with
  `dart format`.
- Widgets are small and single-purpose; extract a widget once a build method
  exceeds roughly 40 lines.
- Prefer `const` constructors wherever possible.
- No business logic in widgets: widgets render state and forward events; logic
  lives in the application layer (see `rules/app-architecture.md`).
- User-facing strings come from the localization bundles in `lib/l10n/`; no
  hard-coded copy in widgets.
- A change is done when `flutter analyze`, `dart format --set-exit-if-changed .`
  and `flutter test` all pass.

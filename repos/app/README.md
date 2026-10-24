# {{ projectName }} — App

Flutter application for **{{ projectName }}**, shipping to Android and iOS on a
fortnightly release train.

## Layout

- `lib/` — Riverpod-layered app code (features, routing, networking)
- `test/` — unit, widget and golden tests
- `integration_test/` — end-to-end flows

## Commands

```bash
flutter pub get
flutter analyze
flutter test
flutter run
```

The workspace contract (`repositories/app.md` and
`conventions/release-train.md`) lists the build rules, the release cadence and
the quick checks the agent runs before calling a change done.

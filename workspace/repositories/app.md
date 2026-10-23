# Repository: app

| | |
| --- | --- |
| Name | `app` |
| Stack | Flutter 3.35 stable / Dart 3.9, Riverpod, go_router, Dio |
| Platforms | Android (minSdk 24, targetSdk 36), iOS 15+ |

## Layout

```
app/
  lib/
    app/           router.dart, flags.dart, theme, l10n wiring
    features/      one folder per feature: presentation/ application/ domain/ data/
    ui/            design-system widgets
    l10n/          localization bundles
  test/            unit and widget tests (mirrors lib/)
  integration_test/  on-device tests
  android/  ios/   platform shells
  fastlane/        store metadata and lanes
```

## Commands

| Task | Command |
| --- | --- |
| Install dependencies | `flutter pub get` |
| Code generation (Riverpod, freezed) | `dart run build_runner build --delete-conflicting-outputs` |
| Static analysis | `flutter analyze` |
| Format check | `dart format --set-exit-if-changed .` |
| Unit and widget tests | `flutter test` |
| Integration tests | `flutter test integration_test` |
| Debug build (Android) | `flutter build apk --debug` |
| Release builds | `flutter build appbundle` and `flutter build ipa` (release manager only) |

Quick check before pushing: `flutter analyze && flutter test`.

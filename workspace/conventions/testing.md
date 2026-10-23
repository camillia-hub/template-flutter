# Testing conventions

- `flutter test` runs the unit and widget tests under `test/`; the suite stays
  under 3 minutes.
- Unit tests cover the application and domain layers: notifiers, use cases and
  repositories (with fakes).
- Widget tests cover every screen's key states: loading, error, empty, content.
- Golden tests (`golden_toolkit`) cover the design-system widgets in `lib/ui/`;
  goldens are regenerated deliberately with `flutter test --update-goldens` and
  reviewed in the PR.
- Mocks are hand-written fakes or `mocktail`; no reflection-based mocking.
- Integration tests in `integration_test/` cover the critical journey (sign in,
  main flow, sign out) and run nightly on CI emulators.
- Coverage floor: 80% lines on `lib/`, enforced in CI.

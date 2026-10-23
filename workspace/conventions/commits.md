# Commit and pull-request conventions

- Conventional Commits: `feat:`, `fix:`, `chore:`, `refactor:`, `test:`, `docs:`,
  `perf:`, scoped by feature — `feat(trips): add tracking map`.
- One logical change per commit; PRs stay under roughly 400 changed lines.
- PRs include screenshots or a screen recording for any UI change, and name the
  feature flag when the change sits behind one.
- Every PR links its task and lists the checks the author ran (`flutter analyze`,
  `flutter test`).
- Squash-merge to `main`.

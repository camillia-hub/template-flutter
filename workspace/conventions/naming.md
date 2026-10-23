# Naming conventions

- Files and directories: `snake_case.dart`; classes: `PascalCase`; members:
  `camelCase`.
- Widgets are named after what they show (`OrderCard`, `HomeScreen`); full-page
  widgets end in `Screen`.
- Riverpod providers end in `Provider` (`tripsProvider`); notifiers end in
  `Notifier`.
- Repositories end in `Repository`; data sources end in `RemoteDataSource` or
  `LocalDataSource`.
- Test files mirror the source tree:
  `test/features/trips/trip_repository_test.dart`.
- Branches: `<type>/<task-id>-<slug>`; commits follow Conventional Commits (see
  `conventions/commits.md`).

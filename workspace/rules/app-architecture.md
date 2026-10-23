# App architecture rules

- State management is Riverpod with code-generated providers; no `setState`
  beyond ephemeral UI state, and no additional state libraries.
- Layers: `presentation` (widgets and providers) -> `application` (use cases and
  notifiers) -> `domain` (entities, repository contracts) -> `data`
  (repositories, DTOs, API and local sources). Dependencies point inward only.
- Repositories are interfaces in `domain/` with implementations in `data/`;
  presentation never touches DTOs.
- Errors surface as typed failures (sealed classes); the UI maps them to
  localized messages. Raw exceptions never cross a layer boundary.
- Navigation uses go_router with routes declared in `lib/app/router.dart`; the
  map in `ui/map.md` must stay in sync.
- Networking goes through the single Dio client in `data/api_client.dart` with
  interceptors for authentication and logging.
- Generated files (`build_runner`: Riverpod, freezed) are build outputs and are
  not committed.

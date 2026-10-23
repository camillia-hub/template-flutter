# Release-train conventions

The app ships on a fortnightly release train.

- Cadence: a release branch `release/YYYY.MM.x` is cut from `main` every second
  Monday; versions are `YYYY.MM.<patch>` (for example `2026.10.1`).
- Code freeze starts at the branch cut. Only fixes for release-blocking defects
  merge into the release branch, cherry-picked from `main` via a PR labelled
  `release-blocker`.
- Everything on `main` must be shippable: unfinished features sit behind feature
  flags in `lib/app/flags.dart`, defaulting to off.
- After the cut, the release candidate soaks on the internal tracks (Play
  internal testing, TestFlight) for 3 days, then rolls out in phases:
  10% -> 50% -> 100%.
- Hotfixes branch from the released tag as `hotfix/<version>`, bump the patch
  version (`2026.10.2`) and merge back to `main`.
- The agent never publishes to the stores; a release manager performs store
  submission and rollout steps manually outside the agent.
- Each train gets release notes in `fastlane/metadata/` and a changelog entry.

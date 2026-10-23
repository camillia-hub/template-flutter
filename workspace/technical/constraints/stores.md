# Store and distribution constraints

- Android ships as an App Bundle to Google Play; iOS as an IPA via TestFlight and
  then the App Store. Both use the fastlane lanes in `fastlane/`.
- Signing keys and store credentials live in the company vault; they never enter
  the repository and the agent never handles them.
- Store submission, phased rollout and any halt of a rollout are performed by the
  release manager manually outside the agent.
- Privacy declarations (Play data safety, App Store privacy labels) are updated
  in the same PR as any change to collected data.
- The app must pass store review at all times: no private APIs, no background
  location without an active trip (see `business/rules.md` BR-4).

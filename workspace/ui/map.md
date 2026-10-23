# UI map

App navigation with go_router, declared in `lib/app/router.dart`. Keep this file
in sync when routes change.

| Route | Screen | Feature | Notes |
| --- | --- | --- | --- |
| `/welcome` | `WelcomeScreen` | auth | first run / signed out |
| `/sign-in` | `SignInScreen` | auth | |
| `/home` | `HomeScreen` | home | map and booking entry |
| `/trip/estimate` | `EstimateScreen` | trip | fare estimate |
| `/trip/active` | `ActiveTripScreen` | trip | live trip state |
| `/trip/:id/receipt` | `ReceiptScreen` | trip | final fare |
| `/history` | `HistoryScreen` | history | past trips |
| `/settings` | `SettingsScreen` | settings | account, payment methods |

Dialogs and sheets are route-less (shown by their parent screen). Deep links:
`https://<app-domain>/trip/<id>` opens `/trip/:id/receipt` when signed in.

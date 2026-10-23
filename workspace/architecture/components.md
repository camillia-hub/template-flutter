# App components

```
+--------------+  HTTPS/JSON  +------------+      +-------------+
| Flutter app  | -----------> | Backend API| ---> | PostgreSQL  |
| (this repo)  | <----------- | (other ws) |      +-------------+
+------+-------+              +------------+
       | push (FCM/APNs)
       v
+--------------+
| Push gateway |
+--------------+
```

| Component | Where | Responsibility |
| --- | --- | --- |
| Flutter app | `app` repository | All client logic; offline-tolerant trip flow. |
| Backend API | separate workspace | Trips, fares, payments, accounts. |
| Push gateway | backend side | Trip status notifications via FCM/APNs. |

The app holds no secrets beyond its public API key; it authenticates with
short-lived tokens refreshed against the backend.

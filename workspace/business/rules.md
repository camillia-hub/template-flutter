# Business rules

Example domain (ride hailing) — adapt during workspace setup.

- BR-1 The fare shown before booking is an estimate; the final fare is computed
  after drop-off and shown before payment capture.
- BR-2 A trip can be cancelled free of charge within 2 minutes of booking;
  afterwards a cancellation fee applies.
- BR-3 Prices are stored as integer minor units with an ISO 4217 currency code.
- BR-4 Location data is collected only while a trip is active and is never shared
  with third parties.
- BR-5 Every payment-relevant event (estimate, capture, refund) writes an audit
  entry.
- BR-6 Features behind flags may not be enabled for more than 10% of users
  without product-owner sign-off.

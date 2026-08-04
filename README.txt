MSS Revenue & Membership Intelligence Center v2.2

Correction:
- Membership plan reporting no longer uses fields that may contain an individual's name.
- Plan name priority:
  1. Explicit Stripe Membership Name / Membership Plan / Subscription Plan fields.
  2. Match Stripe Customer Email to the uploaded Membership Snapshot CSV.
  3. Match Stripe Customer Name to the uploaded Membership Snapshot CSV.
  4. Unspecified Membership when no reliable match exists.
- Added Unmatched Plan Revenue KPI so mapping gaps are visible.
- Product and generic Invoice Description fields are no longer accepted as membership-plan names.

For the strongest matching, upload the current Membership Snapshot CSV before the Stripe Balance History CSV.

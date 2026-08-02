MSS Revenue & Membership Intelligence Center v2.0

Foundation release:
- Renamed product to MSS Revenue & Membership Intelligence Center.
- Reservation CSV remains the rental history/forecast source.
- Membership CSV is treated as a current operational snapshot.
- Added optional Stripe Membership Billing History CSV upload.
- Added Data Source Status panel.
- Added historical membership revenue, paid invoice, failed payment and refund table.
- Current active-member count is driven primarily by Membership Status.
- Membership Start/End fields are not treated as original start/termination dates because they represent billing-cycle dates.
- Historical membership counts require archived snapshots; Stripe provides historical billing/revenue, not exact historical headcount.

Stripe importer is intentionally flexible and recognizes common Stripe Balance History/invoice fields. A facility-specific Stripe file may require a column-mapping refinement after testing.

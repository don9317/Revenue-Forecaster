MSS Revenue & Membership Intelligence Center v3.2

Built against the actual TM Fieldhouse MSS Membership and Stripe Balance History exports supplied September 2026.

Fixes:
- Recognizes MSS 'MRR (Facility Revenue)' as the primary current MRR field.
- Recognizes 'Plan Amount (Facility Revenue)' as the facility-revenue fallback.
- Preserves 'Plan Amount (Billed To Member)' separately.
- Stripe classification now tests Registration/Event before Membership so a registration named
  'Elementary Full Session Membership' remains Registration revenue.
- Direct Stripe membership charges use Description as the membership plan name.
- Stripe membership refund descriptions such as 'REFUND FOR CHARGE (Plan Name)' map back to the plan.
- Retains v3.1 historical rental fallback and centralized revenue engine.

Validation against the supplied MSS Membership Snapshot:
46 active members; $2,309 current facility MRR.


Version 3.3
-----------
- Revenue Breakdown now labels Stripe monthly membership collections as "Actual Membership Revenue."
- The tile note now says "Stripe revenue received during selected month."
- Current Snapshot MRR remains a separate run-rate measure based on active MSS memberships.
- Added an MRR vs. Actual Revenue explanation to the Membership Forecast Center.
- Footer updated to v3.3.

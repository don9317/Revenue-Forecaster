My Sport Space Revenue & Membership Intelligence Center v6.12

DATA-SOURCE INTEGRITY RELEASE

Changes from v6.11:
- Current Membership Snapshot now accepts only a validated MSS Membership Snapshot CSV.
- Stripe Balance History cannot populate Active Members or Current Membership MRR Baseline.
- Invalid/wrong files selected in the Membership upload are rejected with an explanation.
- Removed the duplicate legacy Projected New Members / Avg MRR controls at the top of Memberships.
- Membership — Monthly Forecast is the single source of truth for future membership assumptions.
- Current Membership MRR Baseline is calculated only from active rows in the MSS Membership Snapshot CSV.
- Recurring new MRR carries forward once into future months (no duplicate addition).
- Preserves the v6.11 consolidated Final Forecast graph behavior.

IMPORTANT
Upload the MSS Membership Snapshot CSV in the Membership Upload area and Stripe Balance History in its separate Stripe upload area.

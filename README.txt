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


Version 4.0: presentation redesign with Overview, Revenue, Memberships, Historical, Comparisons and Forecast tabs plus clickable overview tiles and compact Manage Data access. Existing calculation logic retained.


Version 4.1 — Overview Revenue Performance & Forecast
-----------------------------------------------------
Presentation enhancement only; core v3.3/v4.0 reporting logic remains intact.

Added to Overview:
- January–December Revenue Performance & Forecast chart.
- Color-coded lines for Rentals, Memberships, Registrations/Events, and Parties.
- Bold Total Actual Revenue line.
- Dashed Total Forecast line for the remaining year.
- Historical category values use the same centralized actual-revenue sources as the report.
- Future rental forecast uses the existing forecast() engine.
- Future membership forecast uses the existing Membership Forecast Center assumptions.
- Registrations/Events and Parties are not independently projected because the current model does
  not yet contain a separate forward forecasting method for those categories.
- Year-over-year comparison is intentionally reserved until a full prior-year history exists.


Version 4.2 — Navigation & Admin/Data Sources Fix
-------------------------------------------------
- Rebuilt top-tab navigation with delegated click handling.
- Rebuilt Overview navigation-tile click handling.
- Added a dedicated Admin / Data Sources tab.
- Removed upload/data-source controls from the Overview page.
- Reservation, Membership Snapshot, Stripe and other data controls now live under Admin / Data Sources.
- Added defensive chart rendering so a chart issue cannot disable navigation.
- Existing revenue, membership, historical, comparison and forecast calculations remain unchanged.

Version 4.3 — Navigation Repair
- Top navigation buttons are explicit type=button controls with direct click actions.
- Overview intelligence tiles now have direct click actions and keyboard support.
- Navigation controller is exposed globally before initialization to avoid event-binding failures.
- Obsolete Reservation Data / Membership Snapshot / Stripe History strip removed from Overview.
- All upload and source-management controls remain exclusively under Admin / Data Sources.
- Reporting and calculation logic unchanged.


Version 4.4 — Bulletproof Navigation / Clean Overview
------------------------------------------------------
- Navigation no longer depends on JavaScript event initialization.
- Every top navigation button directly switches a body view state.
- Overview tiles use the same direct state switching.
- CSS controls which report sections are visible.
- Overview now shows only the Overview content and compact revenue summary; the long report sections are hidden.
- Revenue, Memberships, Historical, Comparisons and Forecast each show only their own report section.
- Admin / Data Sources exclusively contains uploads, source status and manual revenue inputs.
- Added a visible v4.4 version badge beneath the report title.
- Existing calculations and reporting logic are unchanged.

Version 4.5: File uploads, row counts and coverage diagnostics moved to Admin/Data Sources only. Growth Adjustment Inputs moved off Overview and retained under Forecast. Overview is management-facing only. Calculations unchanged.


Version 4.6 — Section Cleanup
------------------------------
- Data Source Status moved exclusively to Admin / Data Sources.
- Data Source Status removed from Overview and Revenue.
- Growth Adjustment Inputs moved exclusively to Forecast.
- Growth Adjustment Inputs removed from Overview, Revenue and Historical.
- Repaired legacy HTML wrapping around Growth Adjustment Inputs that allowed it to leak into other tabs.
- Reporting calculations remain unchanged.


Version 4.7 — Future Month Adjustment Planner
----------------------------------------------
- Top controls explicitly labeled Facility, Forecast Month, Data / Forecast As-of Date, and Growth Scenario.
- Added Future Month Adjustment Planner to Forecast.
- Toggle between Remaining This Year and Next 12 Months.
- Month-by-month adjustments for Rentals, Memberships, Events and Parties.
- Optional management note/reason for each month.
- System Forecast, Management Adjustments and Final Forecast totals.
- Adjustments are independent by month and stored locally in the browser.
- Overview dashed forecast line incorporates Future Month Planner adjustments.
- Existing reporting calculations otherwise unchanged.

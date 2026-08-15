MSS Revenue & Membership Intelligence Center v3.1

Rental History Fallback:
- Completed/prior rental actuals use Reservation CSV when that period has rental rows.
- If no Reservation rental rows exist for the period, the engine falls back to Stripe Balance History.
- Stripe rental revenue is a fallback, not added to Reservation rental revenue, preventing double counting.
- Revenue Comparison Center uses the same centralized engine for Current and Prior Actual.
- Prior Actual tile identifies the rental source used.
- Stripe category priority remains Membership -> Registration/Event -> Party -> Rental.

# Payment Gateways for a Sole Proprietor LLC (2026)

> Research conducted via Gemini with web search grounding, April 2026.
> Verify current rates at stripe.com, squareup.com, paypal.com, helcim.com, and wise.com before making your decision.

---

## TL;DR Recommendation

**Stripe + Square together** is the safest setup for most solo LLCs. Stripe for online payments, Square as your in-person and backup processor.

---

## Fee Comparison

| Gateway | Online | In-Person | Monthly | ACH |
|---|---|---|---|---|
| **Stripe** | 2.9% + $0.30 | 2.7% + $0.05 | $0 | 0.8% (max $5) |
| **Square** | 3.3% + $0.30 | 2.6% + $0.10 | $0 | 1% (min $1) |
| **PayPal** | 3.49% + $0.49 | 2.29% + $0.09 | $0 | N/A |
| **Helcim** | ~2.3% + $0.25* | ~1.8% + $0.08* | $0 | 0.5% + $0.25 |
| **Wise** | ~1–2.9% | N/A | $0 | Free (local) |
| **Authorize.net** | 2.9% + $0.30 | N/A | $25 | 0.75% |
| **Braintree** | 2.59% + $0.49 | N/A | $0–$100 | 0.75% (max $5) |
| **Stax** | Interchange + subscription | — | $99 | — |

*Helcim uses interchange-plus pricing; rates decrease automatically as volume grows.*

**Chargeback Fees:** Stripe ($15), Square ($0), PayPal ($20), Helcim ($15 — refunded if won), Authorize.net ($25).

**Setup Fees:** $0 for most. Wise has a one-time $31 fee for local banking details.

---

## Best by Use Case

| Use Case | Best Pick | Why |
|---|---|---|
| Best overall | **Stripe** | Most versatile; scales from $0 to $1M+; excellent developer and no-code options |
| In-person / retail | **Square** | Hardware ecosystem; $0 chargeback fee; free POS software |
| Online-only | **Stripe** | Highest checkout conversion via Stripe Link saved-card feature |
| Freelancing / B2B invoicing | **Wise Business** | Lowest fees on large-sum invoices; recurring client billing |
| International payments | **Wise** | Mid-market exchange rates; cheapest multi-currency handling |
| Low volume (<$5k/mo) | **Helcim or Square** | No monthly fees, transparent pricing |
| High volume ($25k+/mo) | **Stax** | $99/mo subscription eliminates percentage markups |

---

## Key Features

- **Invoicing:** All support it. Wise and Helcim offer lowest-fee B2B invoicing for large-sum transactions.
- **Recurring billing / subscriptions:** Stripe Billing is the gold standard. Authorize.net strong for fixed-date monthly subscriptions.
- **POS hardware:** Square leads — full register ecosystem, card readers, Tap to Pay. Stripe Terminal exists but requires integration.
- **Accounting integrations:** All connect to QuickBooks Online and Xero. Stripe and Square have the deepest native sync.

---

## Payout Speed

| Speed | Providers |
|---|---|
| Standard (2 business days) | Stripe, Helcim, Authorize.net |
| Next-day | Square (with Square Checking account) |
| Instant (1.5% fee) | Stripe, Square |
| Real-time | Wise (domestic transfers, often minutes) |

---

## Account Stability & Gotchas

- **PayPal** has the worst track record for freezing funds — avoid as your primary processor.
- **Stripe, Square, and PayPal** all use aggressive automated risk monitoring; velocity spikes can trigger holds.
- New accounts may face a **rolling reserve** (5–10% held for 90 days), especially on Stripe and PayPal.
- The 2026 chargeback threshold has tightened to **0.65%** (down from 1%). High-risk categories: coaching, digital products, travel.

**Mitigation strategies:**
1. Use multi-processor approach — Stripe as primary, Square as backup; never rely on one processor.
2. Enable 3D Secure 2.3 (Stripe, Braintree) to shift fraud liability to the card issuer.
3. Set your business descriptor to match your LLC name exactly — reduces confusion-based chargebacks.
4. For PayPal: link your bank account and run small regular transactions before scaling up volume.

---

## What You Need to Sign Up

- EIN from the IRS
- Articles of Organization (state filing)
- Operating Agreement (proves signing authority)
- SSN + government-issued photo ID (KYC compliance)
- US business bank account (Mercury, Relay, or traditional bank)

**Approval time:** Square and Stripe — instant to 2 hours. Helcim and Authorize.net — 2–3 business days.

---

## Summary

- For most sole proprietor LLCs starting out: **Stripe + Square** together
- **Helcim** is underrated for $5k–$25k/month; interchange-plus with no monthly fee is rare
- **Avoid relying solely on PayPal** for business-critical revenue
- **Wise** is not a full payment gateway but excellent for B2B invoicing and international payments — pair with Stripe for a complete stack

# Playbook 8: Billing & Finance

_Always running. Mostly automated._

---

## Project Billing (AUTO DRAFT → TOM APPROVE)

### Quick Win / Starter
- 50% upfront on contract signature (auto-invoiced via Stripe)
- 50% on delivery (auto-invoiced on sign-off)

### Growth / Scale
- Setup fee: 50% upfront, 50% on delivery
- Monthly retainer: first month due at contract signature
- Recurring via Stripe Billing subscription

### Milestone Billing (Scale tier, large projects)
- Liaison drafts milestone invoices using `templates/invoice.md`
- Tom approves → auto-sent via Stripe

## Recurring Billing (FULLY AUTO)

```
Stripe subscription charges monthly
  → Payment succeeds → receipt sent automatically
  → Payment fails → auto-reminder email
     → Retry 1 (Day 3)
     → Retry 2 (Day 7)
     → Retry 3 (Day 14)
     → After 3 failures → Tom notified, service paused
```

## Expense Tracking (AUTO)

- **Per-client cost tracking:**
  - API costs (Claude, OpenAI — tracked by project/client)
  - Hosting costs (Vercel, VPS allocation)
  - Tool costs (any client-specific subscriptions)
- **Monthly cost report** generated
- **Margin alert** if any client's costs exceed 30% of their retainer

## Bookkeeping

- **Wave** (free) for income/expense tracking
- All Stripe transactions auto-categorized
- Quarterly: review P&L, reconcile accounts
- Annual: hand to CPA for tax filing

## Tax

- **Quarterly estimated payments** — Tom handles (15 min/quarter)
- **Annual filing** — CPA when revenue justifies ($500-1K/year)
- **Track deductibles:** API costs, hosting, software, home office, equipment

## Margin Targets
| Tier | Revenue | Costs | Margin |
|------|---------|-------|--------|
| Starter $149/mo | $149 | ~$25 | 83% |
| Growth $499/mo | $499 | ~$65 | 87% |
| Scale $1,500+/mo | $1,500 | ~$150 | 90% |

## Templates Used
- `templates/invoice.md`

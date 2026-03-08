# Playbook 6: Client Delivery

_Trigger: Build complete, deployed, health checks passing._

---

## Pre-Delivery (AUTO)

1. **Delivery brief generated** — what was built, how it works, key numbers
2. **Demo environment ready** — everything running in production, data flowing
3. **Delivery email sent** to client scheduling the walkthrough call

## Delivery Call (TOM — 15-30 min screen share)

### Structure
1. **Recap** (2 min) — "Here's what you asked for, here's what we built"
2. **Live demo** (10-15 min) — show it working in real-time with their data
3. **Walkthrough** (5 min) — where to find things, how to check status, what to do if something looks off
4. **Questions** (5 min) — answer anything
5. **Sign-off** — verbal or written confirmation they're happy

### What to Show
- The automation running end-to-end
- Output quality (reports, emails, data — whatever it produces)
- Where results land (their existing tools — Sheets, CRM, email, etc.)
- Monitoring dashboard or status page (if applicable)
- How to reach support (support@pulsesystems.com)

### What NOT to Do
- Don't explain the technical architecture (they don't care)
- Don't show the code or workflows (they hired you so they don't have to)
- Don't oversell — show what it does, not what it could do someday

## Post-Delivery (AUTO)

1. **Delivery confirmation email** — summary of what was delivered, support contact, next steps
2. **Retainer activation** — if applicable, recurring Stripe billing starts
3. **30-day check-in scheduled** — "How's everything running?"
4. **Case study draft** — Junior starts drafting based on the project (Tom approves before publishing)
5. **Referral ask** (Day 14) — "Know anyone else who'd benefit from this?"

## Templates Used
- `templates/email-delivery-confirmation.md`
- `templates/email-30day-checkin.md`
- `templates/email-referral-ask.md`

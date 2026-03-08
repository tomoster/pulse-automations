# Playbook 7: Ongoing Support & Maintenance

_Trigger: Client on active retainer._

---

## Automated Monitoring (ALWAYS RUNNING)

- **Health checks** — cron-based scripts check each client's automations (uptime, error rates, output quality)
- **Weekly summary** — auto-generated performance report per client
- **Anomaly alerts** — immediate flag if something breaks or degrades

## Issue Handling (AUTO → TOM ESCALATION)

### Triage Flow
```
Client emails support@pulsesystems.com
  → Junior reads and classifies:
     Bug → route to engineering, fix, deploy, notify client
     Feature request → log, acknowledge, bundle into monthly optimization
     Question → draft response, send (Tom approves if sensitive)
     Urgent/angry → IMMEDIATE Tom notification
```

### Escalation Rules
| Severity | Response Time | Who |
|----------|-------------|-----|
| System down | < 1 hour | Tom notified immediately, auto-fix attempted |
| Bug | < 24 hours | Engineering auto-fixes, Tom notified if unresolved |
| Feature request | < 48 hours | Acknowledged, logged for monthly review |
| Question | < 24 hours | Junior drafts response |
| Unhappy client | < 2 hours | Tom calls directly |

## Monthly Optimization (AUTO + TOM)

1. **Junior analyzes** — usage data, error logs, performance trends
2. **Optimization report drafted** — what's working, what could be better, recommended changes
3. **Tom reviews** (5 min) — approves or adjusts recommendations
4. **Engineering implements** approved changes
5. **Client notified** — "Here's what we improved this month"

## Quarterly Review (TOM — 30 min call)

- Review ROI: time saved, errors prevented, revenue impact
- Discuss expansion: "What else is manual that shouldn't be?"
- Relationship deepening — this is where natural upsells happen
- Adjust scope if needed

## Churn Prevention

Watch for:
- Declining usage (they stopped using what we built)
- No response to monthly reports
- Missed payments (auto-flagged by Stripe)
- Support tickets increasing (system isn't stable)

If any detected → Tom proactive outreach before it becomes a problem.

## Templates Used
- `templates/email-monthly-report.md`
- `templates/email-optimization-summary.md`

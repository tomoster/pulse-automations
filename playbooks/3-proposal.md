# Playbook 3: Proposal & Close

_Trigger: Discovery call completed, workflow audit generated._

---

## Proposal Drafting (AUTO)

1. **Liaison drafts proposal** using `templates/proposal.md`
   - Pulls from: call summary, workflow audit, recommended tier
   - Includes: problem summary, proposed solution, deliverables, timeline, pricing, payment terms
   - Tone: Tom's voice — direct, confident, no buzzwords

2. **Pricing selection** (based on discovery findings):
   | Signal | Recommended Tier |
   |--------|-----------------|
   | Single pain point, simple fix | Quick Win ($500-2K) |
   | 2-3 connected workflows | Starter ($2K-5K build + $149/mo) |
   | Full department overhaul | Growth ($5K-10K + $499/mo) |
   | Multi-department, enterprise needs | Scale ($10K-25K + $1,500+/mo) |

3. **Proposal posted** for Tom's review

## Tom's Role

- Review proposal (5 min) — adjust pricing, scope, or language if needed
- Approve → auto-sent to client via email with e-sign link
- If negotiation needed → Tom handles directly, updates proposal, re-sends

## Contract (AUTO once proposal accepted)

- PandaDoc generates contract from `templates/contract.md`
- Standard terms: 50% upfront for project work, first month retainer due at signing
- E-sign link included
- On signature → triggers onboarding sequence (Playbook 4)
- On signature → Stripe invoice generated and sent

## Follow-Up Sequence (AUTO if no response)

- Day 2: "Just checking in — any questions about the proposal?"
- Day 5: "Wanted to make sure this didn't get buried. Happy to jump on a quick call."
- Day 10: "No worries if the timing isn't right. I'll check back in a month."
- Day 30: Final check-in, then archive lead

## Templates Used
- `templates/proposal.md`
- `templates/contract.md`
- `templates/email-followup-1.md`
- `templates/email-followup-2.md`
- `templates/email-followup-3.md`

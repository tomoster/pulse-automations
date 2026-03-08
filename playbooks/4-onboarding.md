# Playbook 4: Client Onboarding

_Trigger: Contract signed, first payment received._

---

## Onboarding Sequence (AUTO)

### Email 1: Welcome (Immediately on signature)
- Template: `templates/email-welcome.md`
- What to expect, timeline, next steps
- "We'll send you a short form to collect what we need to get started"

### Email 2: Onboarding Form (Day 1)
- Template: `templates/email-onboarding-form.md`
- Link to Tally.so form collecting:
  - Business context (industry, size, revenue range)
  - Current tools (CRM, email, scheduling, billing — everything)
  - Workflow descriptions (what they do manually, step by step)
  - Access credentials (logins, API keys — stored securely)
  - Priority ranking (what hurts most → what can wait)
  - Preferred communication (email, Slack, text)

### Email 3: Kick-off Confirmation (After form submitted)
- Template: `templates/email-kickoff.md`
- Confirms scope, timeline, and next steps
- For Growth/Scale: includes Calendly link for kick-off call

## Project Setup (AUTO)

1. **Create client repo** from `templates/project-scaffold/`
   ```
   gh repo create pulse-client-[name] --private --template pulse-automations/templates/project-scaffold
   ```
2. **Populate CLAUDE.md** — minimal, corrections only
3. **Create .env** with client credentials from onboarding form
4. **Generate project brief** — markdown doc compiling all onboarding data
5. **Confirm scope matches proposal** — flag any gaps to Tom

## Kick-off Call (TOM — Growth/Scale only, 15 min)

- Quick alignment on priorities
- Answer any questions
- Build confidence: "Here's exactly what happens next"
- NOT a re-discovery — that's already done

## Handoff to Engineering

- Project brief → Junior → Architect (Playbook 5)
- Include: onboarding form data, call notes, proposal scope, access credentials location

## Templates Used
- `templates/email-welcome.md`
- `templates/email-onboarding-form.md`
- `templates/email-kickoff.md`
- `templates/project-scaffold/`

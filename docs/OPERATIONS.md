# Pulse Systems — Operations Blueprint

_The complete operating system. Every department, every workflow, every tool. What's automated, what needs Tom._

---

## Company Overview

**What Pulse does:** Takes manual business workflows and replaces them with AI-powered systems. Not SaaS — custom, owned automations built for each client.

**How it runs:** One human (Tom) + an AI operations team (Junior + specialized agents). Tom is the face, relationship holder, and final quality gate. Everything else is delegated down.

**Revenue model:** Project-based builds → monthly retainers for maintenance/expansion. Land with a quick win ($500-2K), expand into recurring ($500-1,500/mo).

---

## The Client Journey (End to End)

```
Lead comes in
  → Intake & qualification (AUTO)
  → Discovery call (TOM)
  → Workflow audit / free assessment (AUTO + TOM REVIEW)
  → Proposal & pricing (AUTO DRAFT → TOM APPROVE)
  → Contract & payment (AUTO)
  → Onboarding & access collection (AUTO)
  → Build (AGENTS → TOM QA)
  → Delivery & walkthrough (TOM)
  → Support & maintenance (AUTO + TOM ESCALATION)
  → Billing (AUTO)
  → Expansion / upsell (AUTO FLAG → TOM RELATIONSHIP)
```

---

## Department 1: Marketing & Lead Generation

**Purpose:** Get leads into the pipeline without Tom manually prospecting.

### Channels
| Channel | Method | Automation Level |
|---------|--------|-----------------|
| **Website** | SEO + "Free Audit" CTA → email capture | ✅ Fully auto |
| **LinkedIn** | Content posts (2-3x/week), comment engagement, DM outreach | ⚠️ HITL — Tom posts, Junior drafts |
| **Referrals** | Happy client → intro email template | ⚠️ HITL — Tom sends |
| **Cold outreach** | Targeted email sequences to SMBs showing manual workflow pain | ✅ Auto sequences, Tom approves templates |
| **Content** | Blog posts, case studies, LinkedIn articles | ⚠️ HITL — Junior drafts, Tom approves |

### Agent: Content
- Drafts LinkedIn posts in Tom's voice (post-x / post-linkedin skills)
- Writes case studies from completed project data
- Never posts without Tom's approval

### Tools
- **Website:** Vercel (hosting), email capture form → Supabase
- **LinkedIn:** Manual posting (Tom's account)
- **Email sequences:** Loops.so or Resend (transactional + sequences)
- **CRM:** Pulse CRM (already built at ~/projects/pulse-crm) or Attio (if scaling)

### What Tom Does
- Posts on LinkedIn (from Junior's drafts)
- Sends referral asks to happy clients
- Approves cold outreach templates
- Engages in comments (first 60 min after posting — golden hour)

---

## Department 2: Sales & Intake

**Purpose:** Qualify leads, run discovery, close deals. Tom only talks to qualified prospects.

### Workflow

```
1. Lead submits "Free Audit" form on website
   → AUTO: Confirmation email sent instantly
   → AUTO: Lead data saved to CRM
   → AUTO: Junior analyzes their business (website, LinkedIn, public info)
   → AUTO: Pre-call brief generated for Tom

2. Discovery call (15-30 min) — TOM
   → Tom listens, asks about pain points, current tools, budget
   → Takes rough notes or records call

3. Post-call processing — AUTO
   → Junior summarizes call notes
   → Generates workflow audit (what's manual, estimated time waste, opportunity)
   → Drafts proposal with pricing

4. Proposal sent — TOM APPROVE → AUTO SEND
   → Liaison drafts proposal (draft-proposal skill)
   → Tom reviews, adjusts pricing if needed, approves
   → Auto-sent via email with e-sign link

5. Contract & payment — AUTO
   → E-sign via DocuSign or PandaDoc
   → First payment via Stripe invoice (auto-generated)
   → Onboarding sequence triggered on signature
```

### Agent: Liaison
- Drafts all external communications (emails, proposals, invoices)
- Never sends without Tom's approval
- Uses Tom's voice and context from CRM

### Pricing Structure
| Tier | One-Time Build | Monthly Retainer | What's Included |
|------|---------------|-----------------|-----------------|
| **Quick Win** | $500-2,000 | — | Single automation (e.g., auto-responses, form processing, report generation) |
| **Starter** | $2,000-5,000 | $149/mo | 2-3 connected automations + monthly maintenance |
| **Growth** | $5,000-10,000 | $499/mo | Full workflow overhaul + personal AI assistant + weekly optimization |
| **Scale** | $10,000-25,000 | $1,500+/mo | Enterprise-grade multi-department automation + dedicated support |

**Pricing philosophy:** Start with project-based to build credibility. Convert to retainer after first delivery. First month retainer due upfront for new clients.

### Tools
- **Proposals:** PandaDoc or Google Docs template (Liaison fills, Tom approves)
- **E-sign:** PandaDoc (built-in) or DocuSign
- **Payments:** Stripe (invoicing + subscriptions for retainers)
- **CRM:** Track deal stage, notes, next action

### What Tom Does
- Takes discovery calls (15-30 min each)
- Reviews and approves proposals
- Negotiates pricing when needed
- Relationship management — Tom is the trust anchor

---

## Department 3: Onboarding

**Purpose:** Collect everything needed to build without back-and-forth.

### Workflow

```
1. Contract signed → AUTO trigger onboarding sequence

2. Welcome email — AUTO
   → What to expect, timeline, what we need from them
   → Link to onboarding form

3. Onboarding form — AUTO
   → Business context (industry, size, tools they use)
   → Access credentials (CRM logins, email access, API keys)
   → Current workflow description (what they do manually)
   → Priority ranking (what hurts most)
   → Stored securely in project vault

4. Kick-off summary — AUTO DRAFT → TOM REVIEW
   → Junior compiles form data into a project brief
   → Confirms scope matches proposal
   → Flags any gaps or access issues

5. Kick-off call (optional, 15 min) — TOM
   → Only if project is Growth tier or above
   → Quick alignment, answer questions, build confidence
```

### Tools
- **Onboarding form:** Tally.so or Typeform (free tier works)
- **Credential storage:** 1Password vault (shared per client) or Supabase encrypted
- **Project brief:** Auto-generated markdown → stored in client project folder

### What Tom Does
- Reviews kick-off summary (2 min)
- Optional kick-off call for larger projects
- That's it — everything else is automated

---

## Department 4: Engineering (Build & Delivery)

**Purpose:** Actually build the automations. This is where the agents do real work.

### Workflow

```
1. Project brief lands → AUTO
   → Junior routes to Architect

2. Architect writes technical spec — AUTO
   → What to build, tech stack, integrations needed
   → Spec posted for Tom's approval (quick wins skip this)

3. Tom approves spec — TOM (30 sec - 5 min)

4. Build begins — AUTO
   → Architect routes to Backend/Frontend/Automations agents
   → Agents build in isolated project repos
   → Each agent follows its build skill (backend-build, frontend-build, automations-build)

5. QA — AUTO + TOM
   → Automated tests run
   → Junior reviews output against spec
   → Tom does final walkthrough (5-15 min)

6. Delivery — TOM
   → Tom walks client through the build (15-30 min screen share)
   → Shows them how it works, answers questions
   → Gets sign-off
```

### Agents
| Agent | Role | Automation |
|-------|------|-----------|
| **Architect** | Writes specs from project briefs | ✅ Fully auto (Tom approves spec) |
| **Backend** | APIs, databases, server logic, integrations | ✅ Fully auto |
| **Frontend** | UI, dashboards, client-facing interfaces | ✅ Fully auto |
| **Automations** | Workflows, integrations, n8n/code-based automations | ✅ Fully auto |
| **Junior** | Orchestrates, QAs, flags issues | ✅ Fully auto |

### Tech Stack (Per Project Type)
| Project Type | Stack |
|-------------|-------|
| **Websites** | Next.js / HTML+CSS+JS, Vercel hosting |
| **Automations** | Python scripts, n8n (last resort), cron jobs |
| **AI Assistants** | OpenClaw or custom agent, Claude/GPT API |
| **Dashboards** | Next.js + Supabase, Vercel hosting |
| **Integrations** | Direct API connections, webhooks, MCP servers |

### Tools
- **Code:** Claude Code, Codex (agents use these as tools)
- **Repos:** GitHub (one repo per client project)
- **Hosting:** Vercel (frontend), Hostinger VPS (backend/automations)
- **Databases:** Supabase (default), SQLite (lightweight)

### What Tom Does
- Approves specs (30 seconds for quick wins, 5 min for complex)
- Final QA walkthrough (5-15 min)
- Delivers to client (15-30 min screen share)

---

## Department 5: Client Support & Maintenance

**Purpose:** Keep systems running, handle issues, expand scope.

### Workflow

```
Retainer clients:

1. Monitoring — AUTO
   → Automated health checks on deployed systems (uptime, error rates)
   → Weekly performance summary generated
   → Anomalies flagged immediately

2. Issue handling — AUTO → TOM ESCALATION
   → Client emails support@pulsesystems.com
   → Junior triages: is it a bug, a feature request, or a question?
   → Bugs: auto-routed to engineering, fix deployed, client notified
   → Feature requests: logged, bundled into monthly optimization
   → Questions: Junior drafts response, Tom approves if sensitive

3. Monthly optimization — AUTO + TOM REVIEW
   → Junior analyzes usage data, identifies improvement opportunities
   → Drafts optimization report for client
   → Tom reviews, approves changes
   → Engineering implements approved changes

4. Quarterly review — TOM
   → 30-min call with client
   → Review ROI, discuss expansion, deepen relationship
   → This is where upsells happen naturally
```

### Escalation Matrix
| Issue Type | First Response | Escalation |
|-----------|---------------|-----------|
| System down | AUTO fix attempt → Tom notified | Tom contacts client within 1 hour |
| Bug report | AUTO triage + engineering fix | Tom notified if >24h unresolved |
| Feature request | AUTO logged + acknowledged | Bundled into monthly optimization |
| Billing question | AUTO response from templates | Tom if disputed |
| Unhappy client | IMMEDIATE Tom notification | Tom calls within 2 hours |

### Tools
- **Support email:** support@pulsesystems.com → routed through Junior
- **Monitoring:** Custom health check scripts (cron-based), Vercel analytics
- **Issue tracking:** GitHub Issues (per client repo) or linear.app
- **Client communication:** Email (Liaison drafts, Tom approves)

### What Tom Does
- Handles escalations (rare if systems are solid)
- Quarterly review calls (30 min per client)
- Approves sensitive responses
- Relationship maintenance — this is where retention happens

---

## Department 6: Finance & Billing

**Purpose:** Get paid, track costs, stay profitable.

### Workflow

```
1. Initial invoice — AUTO
   → Generated on contract signature
   → Sent via Stripe
   → First month + setup fee due upfront

2. Recurring billing — AUTO
   → Stripe subscription for retainer clients
   → Auto-charges monthly
   → Failed payment → auto-reminder sequence (3 attempts)
   → After 3 failures → Tom notified

3. Project billing — AUTO DRAFT → TOM APPROVE
   → Milestone-based invoicing for larger builds
   → Liaison drafts invoice (draft-invoice skill)
   → Tom approves, auto-sent

4. Expense tracking — AUTO
   → API costs (Claude, OpenAI, hosting) tracked per client
   → Monthly cost report generated
   → Margin alerts if costs exceed 30% of retainer

5. Tax prep — MANUAL (for now)
   → QuickBooks or Wave for bookkeeping
   → Quarterly estimated tax payments
   → Annual filing (CPA when revenue justifies it)
```

### Pricing Margin Targets
| Tier | Monthly Revenue | Estimated Costs | Target Margin |
|------|----------------|-----------------|--------------|
| Starter ($149/mo) | $149 | ~$20-30 (API + hosting) | 80%+ |
| Growth ($499/mo) | $499 | ~$50-80 | 85%+ |
| Scale ($1,500+/mo) | $1,500+ | ~$100-200 | 87%+ |

Costs are almost entirely API calls and hosting. No employees, no office, no benefits. The margin structure is exceptional for a services business.

### Tools
- **Invoicing:** Stripe Invoicing (auto-generates, tracks payment status)
- **Subscriptions:** Stripe Billing (auto-recurring for retainers)
- **Bookkeeping:** QuickBooks Self-Employed or Wave (free)
- **Expense tracking:** Per-client API cost tracking (custom script or AgentLedger when built)
- **Tax:** Quarterly estimates → CPA for annual filing

### What Tom Does
- Approves non-standard invoices
- Reviews monthly margin report (5 min)
- Quarterly tax payments
- Nothing else — Stripe handles collection

---

## Department 7: Internal Operations

**Purpose:** Keep the machine running. Junior handles this entirely.

### What Runs Automatically
| Function | Frequency | Agent |
|----------|-----------|-------|
| Research pipeline (7 streams) | Nightly | Junior + Gemini |
| Strategy session | Nightly | Junior |
| KB ingestion and push | Nightly | Claude Code |
| Memory maintenance | Every 3 days | Junior |
| Active tasks cleanup | Every 3 days | Haiku |
| File cleanup | Weekly | Haiku |
| Ops health check | Weekly | Ollama |
| Update checker | 2x daily | Ollama/Haiku |
| WeatherClaw improvement | Nightly | Claude Code |

### What Tom Does
- Nothing. This runs without him.

---

## Full Tool Stack

| Category | Tool | Cost | Purpose |
|----------|------|------|---------|
| **Hosting** | Vercel | Free-$20/mo | Frontend hosting |
| **Hosting** | Hostinger VPS | ~$10/mo | Backend, automations, n8n |
| **Database** | Supabase | Free-$25/mo | Client project databases |
| **Payments** | Stripe | 2.9% + $0.30/txn | Invoicing, subscriptions |
| **Email** | Google Workspace | $6/mo | tom@pulsesystems.com, support@ |
| **E-sign** | PandaDoc | Free-$19/mo | Proposals, contracts |
| **Forms** | Tally.so | Free | Onboarding, assessment |
| **CRM** | Pulse CRM (custom) | $0 | Lead tracking, deal pipeline |
| **AI APIs** | Anthropic, OpenAI, Google | ~$50-200/mo | Agent operations |
| **Code** | GitHub | Free | Client project repos |
| **Monitoring** | Custom scripts | $0 | System health checks |
| **Bookkeeping** | Wave | Free | Accounting |
| **Scheduling** | Calendly | Free | Discovery calls |
| **Domain** | pulseequities.com / systems.pulseequities.com | Owned | Website |

**Estimated fixed overhead:** ~$50-100/mo before any clients. Scales to ~$200-300/mo with 10+ clients.

---

## Tom's Weekly Time Budget

| Activity | Time/Week | Notes |
|----------|----------|-------|
| Discovery calls | 1-3 hrs | 2-4 calls × 30 min |
| Spec approvals | 30 min | Quick scans |
| QA walkthroughs | 1-2 hrs | Final check before delivery |
| Client deliveries | 1-2 hrs | Screen share walkthroughs |
| LinkedIn content | 30 min | Review Junior's drafts, post |
| Proposal reviews | 30 min | Approve/adjust pricing |
| Support escalations | 30 min | Rare if systems are solid |
| Quarterly reviews | 30 min | 1 per client per quarter |
| **Total** | **5-10 hrs/week** | **At 5-10 active clients** |

Everything else is automated. As the client base grows, the only thing that scales linearly is discovery calls and delivery walkthroughs. Everything else stays flat.

---

## What's Missing (Action Items)

- [ ] **LLC filing** — file before first paying client
- [ ] **Stripe account** — set up under Pulse Systems
- [ ] **Google Workspace** — tom@pulsesystems.com + support@
- [ ] **PandaDoc** — proposal + contract templates
- [ ] **Calendly** — linked from website CTA
- [ ] **Tally.so** — onboarding form built
- [ ] **Proposal template** — in builds/templates/ (Liaison skill references this)
- [ ] **Invoice template** — in builds/templates/
- [ ] **Contract template** — standard services agreement
- [ ] **Onboarding email sequence** — 3 emails (welcome, form link, kick-off)
- [ ] **Client project folder structure** — standardize per-client repo layout
- [ ] **Support email routing** — support@pulsesystems.com → Junior triage
- [ ] **Health check scripts** — per-client monitoring (cron-based)
- [ ] **Cost tracking per client** — API usage attribution (AgentLedger MVP would solve this)

---

## The Bottom Line

With 5 retainer clients at Growth tier ($499/mo):
- **Monthly revenue:** $2,495 recurring + project fees
- **Monthly costs:** ~$150 (tools + API)
- **Monthly profit:** ~$2,345
- **Tom's time:** ~7 hrs/week

With 10 clients across tiers:
- **Monthly revenue:** $5,000-8,000 recurring
- **Monthly costs:** ~$250
- **Monthly profit:** $4,750-7,750
- **Tom's time:** ~10 hrs/week

The marginal cost of each new client is almost zero. The marginal time is ~1 hr/week (one discovery call + one delivery). That's the whole point.

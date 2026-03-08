# Playbook 5: Engineering Build

_Trigger: Project brief completed from onboarding._

---

## Spec Phase (AUTO → TOM APPROVE)

1. **Junior routes brief to Architect**
2. **Architect writes technical spec:**
   - What to build (specific automations, integrations, UIs)
   - WAT mapping: which workflows to create, which tools to build
   - Tech stack selection (from standard options in OPERATIONS.md)
   - Integration points (client's existing tools → new automations)
   - Deployment target (trigger.dev, Vercel, VPS cron)
   - Estimated build time
   - Edge cases and failure modes

3. **Quick Wins skip spec** — brief is enough, go straight to build
4. **Starter/Growth/Scale** — spec posted for Tom's approval (30 sec - 5 min)

## Build Phase (AUTO)

1. **Architect routes to agents:**
   - Backend agent: APIs, database, server logic, integrations
   - Frontend agent: dashboards, client-facing UI
   - Automations agent: WAT workflows + tools, cron jobs, integrations

2. **Agents build in client repo** following WAT structure:
   ```
   workflows/     # Markdown SOPs for each automation
   tools/         # Python scripts for execution
   .tmp/          # Intermediate files
   .env           # Client credentials (gitignored)
   CLAUDE.md      # Minimal — corrections only
   ```

3. **Self-improvement loop runs:**
   - First pass: build and run → expect errors
   - Agent reads error → fixes tool → updates workflow
   - 2-3 iteration cycles before stable
   - Each cycle makes the automation more robust

4. **CLAUDE.md rule:** Never auto-generate. Only add corrections for consistent agent mistakes that can't be fixed by restructuring code.

## QA Phase (AUTO + TOM)

1. **Automated tests** — agent writes and runs tests against the build
2. **Junior reviews** — output checked against spec, edge cases tested
3. **Tom walkthrough** (5-15 min) — final quality gate:
   - Does it actually work end-to-end?
   - Is the output clean and professional?
   - Would I be proud to show this to the client?

## Deploy Phase (AUTO)

1. **Deploy W + T only** — deterministic code goes to production
   - trigger.dev for scheduled jobs
   - Vercel for frontend/dashboards
   - VPS cron for always-on automations
2. **Agent layer NOT deployed** (exception: Growth/Scale with live AI assistant)
3. **Health check scripts** configured for monitoring
4. **Deployment verified** — run in production, confirm outputs match QA

## Handoff to Delivery (Playbook 6)

- Build complete, deployed, health checks green
- Junior prepares delivery brief: what was built, how it works, how to use it
- Tom schedules delivery call with client

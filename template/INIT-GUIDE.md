# Project Initialization Guide

This guide is for the AI agent helping a user initialize a new project from this template. Follow the phases below in order. Each phase should be a collaborative conversation with the user — ask questions, propose content, and iterate until the user is satisfied before moving on.

---

## Phase 1: Fill Immediately (Project Kickoff)

These documents define *what* the project is. Fill them in the first session.

### 1. SPEC.md

Start here. This drives everything else.

Work through each section with the user:
- **Problem Statement** — What problem are we solving? Why now?
- **Goals / Non-Goals** — Agree on scope boundaries early to prevent creep
- **Requirements** — Functional and non-functional
- **Constraints** — What limits the solution space?
- **Success Criteria** — How do we know we're done? Must be objectively verifiable.
- **Open Questions** — Capture unknowns. Resolve before Phase 2.

**Tip:** If the user has a vague idea, help them sharpen it. Ask "what would success look like?" and "what should this explicitly *not* do?" For early-stage projects, keep requirements high-level and put uncertainty in Open Questions rather than guessing at details. The spec will be refined as the project matures.

### 2. README.md

Fill the project header and overview:
- Title, status ("Phase 1 — Spec"), goal, dates
- Overview (2-3 paragraphs summarizing the project)
- Development repository (working directory, git branch — use "TBD" if not created yet)
- Related projects (if any)

Leave these sections skeletal for now — they'll solidify after DESIGN.md:
- Core Concepts
- Implementation Phases

### 3. AGENT-warm-up.md

Only replace the two marked `{{placeholders}}`. The rest of the file (the "How This Project Works" section) is standard workflow instructions shared across all projects — leave it as-is.

- Project title (`{{PROJECT_TITLE}}`)
- Key codebase location (`{{path to source code...}}` — use "TBD — project is in spec/design phase" if no code exists yet; update when the repo is created)

This takes 30 seconds but is essential for agent continuity from session 1 onward.

### 4. HANDOFF.md

Set the minimal status so future agents reading it aren't confused by placeholders:
- Project title and start date
- Current Status: "Spec phase — defining requirements"
- Phase checklist: use these default milestones until IMPLEMENTATION-GUIDE.md defines real ones:
  > - ⬜ Spec drafted
  > - ⬜ Spec finalized (open questions resolved)
  > - ⬜ Design complete
  > - ⬜ Implementation guide ready
  > - ⬜ Prototype working
  > - ⬜ Tests passing
  > - ⬜ End-to-end demo
- Next Actions: "Finalize SPEC.md, then move to DESIGN.md"
- Session logs: add an inline entry for this initialization session (e.g., "Session 1: Project kickoff — drafted spec, initialized docs"). No need to create a separate log file in `logs/` yet — formal session log files start when development work begins in Phase 2+.

Leave "What We Have" and "Key Design Decisions" empty — they'll be filled in Phase 2.

---

## Phase 2: Fill After Spec Is Agreed (Before Coding Starts)

These documents define *how* to build it. May take one or more sessions.

### 5. DESIGN.md

Work through the architecture with the user:
- **Design Philosophy** — Guiding principles (e.g., "simplicity first", "validate before optimize")
- **Architecture Overview** — Draw an ASCII diagram of the system
- **Key Design Decisions** — For each decision, document the choice, alternatives considered, and rationale
- **Data Model** — Key structures, protocols, or APIs

**Tip:** If there are open questions from SPEC.md, resolve them here. Update SPEC.md as questions are closed.

### 6. IMPLEMENTATION-GUIDE.md

Fill enough detail to start coding:
- Prerequisites and build environment
- File structure (planned, not just existing)
- Phase 1 implementation steps with enough detail to be actionable
- Build & test commands

Later phases can be listed as placeholders — they'll be filled as the project progresses.

### 7. HANDOFF.md (full initialization)

Now flesh out the handoff package with implementation details:
- Current Status updated with design completion
- Replace the default phase checklist with real milestones from IMPLEMENTATION-GUIDE.md
- Next Actions (first coding task)
- Session log entries for the kickoff and design sessions

From this point on, the agent updates HANDOFF.md at the end of every session and creates formal session log files in `logs/`.

### 8. README.md (revisit)

Now that DESIGN.md exists, go back and fill in:
- Core Concepts (extracted from DESIGN.md, written for a newcomer)
- Implementation Phases (from IMPLEMENTATION-GUIDE.md)

---

## Phase 3: Fill Later (As Development Progresses)

### 9. TESTING-GUIDE.md

Fill when the first tests are written. Include:
- Quick start command
- Test inventory table
- Expected output
- Add troubleshooting entries as issues are discovered

### 10. Session Logs

The agent creates a new log for each working session by following the structure in `logs/SESSION-LOG-TEMPLATE.md`. Save each log as `logs/YYYY-MM-DD-session-NN-slug.md`.

Keep the last 5 session logs linked in HANDOFF.md. When it exceeds 5, move older entries to a HANDOFF-ARCHIVE.md (create it when needed).

---

## Checklist

Use this to track initialization progress:

**Phase 1 — Project Kickoff:**
- [ ] SPEC.md — problem, goals, requirements, constraints, success criteria
- [ ] README.md — header, overview, repository
- [ ] AGENT-warm-up.md — project title, codebase path
- [ ] HANDOFF.md (minimal) — project title, start date, status set to "Spec phase"

**Phase 2 — Design & Planning:**
- [ ] DESIGN.md — philosophy, architecture, decisions, data model
- [ ] IMPLEMENTATION-GUIDE.md — prerequisites, file structure, Phase 1 steps, build commands
- [ ] HANDOFF.md (full) — real milestones, next actions, session logs
- [ ] README.md revisited — core concepts, implementation phases

**Phase 3 — Ongoing:**
- [ ] TESTING-GUIDE.md — filled when first tests exist

**Cleanup:**
- [ ] Delete this file (INIT-GUIDE.md) after Phase 2 is complete (all structural docs are filled and coding can begin)

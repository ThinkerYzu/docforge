## {{PROJECT_TITLE}} — Continuation

All project documents are in the same directory as this file. Read these to get up to speed:

1. **`README.md`** — project overview, doc index, and recent updates.
2. **`HANDOFF.md`** — full handoff package: current status, next actions, session history, design decisions. Start with "Current Status" and "Next Actions" at the top.

These documents link to everything else you'll need (session logs, design docs, spec, test guide). Follow the links as needed for the specific task the user gives you.

Key codebase location: `{{path to source code, or "TBD — project is in spec/design phase" if no code yet}}`.

---

## How This Project Works

This project follows a **spec/doc-driven development process**. The documents in this directory are the source of truth — not just records, but the specifications and plans that drive implementation.

### If INIT-GUIDE.md exists

The project is still being initialized. Read `INIT-GUIDE.md` and follow it to complete the setup with the user before starting any implementation work.

### Doc-Driven Workflow

1. **Before coding:** Check [SPEC.md](SPEC.md) for requirements and [DESIGN.md](DESIGN.md) for architecture. Implementation must align with these documents. If something needs to change, update the doc first, discuss with the user, then implement.
2. **During coding:** Follow the plan in [IMPLEMENTATION-GUIDE.md](IMPLEMENTATION-GUIDE.md). When you discover something that contradicts or extends the design, update the relevant doc.
3. **End of every session:**
   - Create a session log in `logs/` (see `logs/SESSION-LOG-TEMPLATE.md` for the format)
   - Update [HANDOFF.md](HANDOFF.md) — current status, phase checklist, next actions, and link to the new session log
   - Keep last 5 session logs in HANDOFF.md; move older ones to HANDOFF-ARCHIVE.md

### Document Hierarchy

| Document | Role |
|----------|------|
| **SPEC.md** | *What* to build and *why* — requirements, constraints, success criteria |
| **DESIGN.md** | *How* to build it — architecture, decisions, data model |
| **IMPLEMENTATION-GUIDE.md** | *Code-level how* — file structure, build steps, phase details |
| **HANDOFF.md** | *Where we are* — current status, next actions, session history |
| **TESTING-GUIDE.md** | *How to verify* — test procedures, expected output |
| **README.md** | *Entry point* — overview, doc index, maintenance guidelines |

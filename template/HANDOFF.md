# Handoff: {{PROJECT_TITLE}}

**Project:** {{PROJECT_TITLE}}
**Started:** {{YYYY-MM-DD}}

---

## Navigation

**Project Docs:** [README](README.md) | [SPEC](SPEC.md) | [DESIGN](DESIGN.md) | [IMPLEMENTATION-GUIDE](IMPLEMENTATION-GUIDE.md) | [HANDOFF](HANDOFF.md) *(you are here)*

**Quick Jump:** [Current Status](#current-status) | [Next Actions](#next-actions) | [Session Logs](#session-logs)

---

## Current Status

**Phase:** {{current phase and completion status}}
**Progress:** {{what has been accomplished}}
**Next Milestone:** {{what we're working toward next}}
**Blockers:** None

> **Phase checklist:**
> - ⬜ Spec drafted
> - ⬜ Spec finalized (open questions resolved)
> - ⬜ Design complete
> - ⬜ Implementation guide ready
> - ⬜ Prototype working
> - ⬜ Tests passing
> - ⬜ End-to-end demo
>
> *Replace with project-specific milestones from IMPLEMENTATION-GUIDE.md in Phase 2.*

### What We Have

{{Leave empty until Phase 2.}}

### Key Design Decisions

{{Leave empty until Phase 2.}}

---

## Next Actions

{{Prioritized list of what to do next. Each item should be actionable.}}

1. **{{Action}} (NEXT.)**  {{description and rationale}}
2. **{{Action}}**  {{description and rationale}}

**Deferred:**
- {{item deferred and why}}

---

## Session Logs

<!-- Phase 1: use inline entries (no log file needed). Phase 2+: link to logs/YYYY-MM-DD-session-NN-slug.md -->

1. **Session 1: {{title}}** ({{YYYY-MM-DD}}) — {{one-line summary}}

---

## Document Web

**Related Documents:**
- [SPEC.md](SPEC.md) - Requirements and constraints
- [DESIGN.md](DESIGN.md) - Architecture and design decisions
- [IMPLEMENTATION-GUIDE.md](IMPLEMENTATION-GUIDE.md) - Code-level details
- [README.md](README.md) - Project overview

**When adding new entries:**
- Create new session log in `logs/` directory
- Update [Session Logs](#session-logs) section with link (keep last 5; move older to archive)
- Update [Current Status](#current-status) with progress
- Regenerate HTML: `./scripts/convert_kb.sh`

---

**Last Updated:** {{YYYY-MM-DD}}

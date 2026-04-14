# Docforge

A doc-driven development template for AI-assisted projects. Copy the `template/` directory to start a new project, then work with an AI agent to progressively fill in the documents through collaborative conversation.

## Quick Start

1. Copy the template into a new project directory:

   ```bash
   cp -r docforge/template my-new-project
   ```

2. Start a conversation with your AI agent and ask it to read `AGENT-warm-up.md`:

   > "Read my-new-project/AGENT-warm-up.md"

3. The agent detects `INIT-GUIDE.md` and walks you through a structured initialization process, starting with defining the project spec.

**This is the same step you repeat every session.** `AGENT-warm-up.md` is the single entry point for the agent -- on the first session it triggers initialization; on subsequent sessions it loads project context and points the agent to `HANDOFF.md` for current status.

## What's in the Template

```
template/
  AGENT-warm-up.md          # Agent reads this at the start of every session
  INIT-GUIDE.md             # Step-by-step initialization instructions (deleted after setup)
  SPEC.md                   # What to build: problem, goals, requirements, constraints
  DESIGN.md                 # How to build it: architecture, decisions, data model
  IMPLEMENTATION-GUIDE.md   # Code-level details: file structure, build steps, phases
  HANDOFF.md                # Current status, next actions, session history
  TESTING-GUIDE.md          # Test procedures and expected output
  README.md                 # Project overview and doc index
  logs/                     # Per-session development logs go here
    SESSION-LOG-TEMPLATE.md # Format template that the agent follows when creating session logs
```

## How the Process Works

The initialization follows three phases, each a conversation between you and the agent.

### Phase 1 -- Project Kickoff (First Session)

You and the agent define *what* the project is:

- **SPEC.md** -- The agent asks you about the problem, goals, non-goals, requirements, constraints, and success criteria. This is the most important document; everything else flows from it.
- **README.md** -- Project header and overview.
- **AGENT-warm-up.md** -- Two placeholders replaced: project title and codebase path.
- **HANDOFF.md** -- Minimal status set so future sessions have context.

### Phase 2 -- Design & Planning (Before Coding)

You and the agent define *how* to build it:

- **DESIGN.md** -- Architecture, key design decisions with rationale, data model.
- **IMPLEMENTATION-GUIDE.md** -- Prerequisites, file structure, actionable implementation steps.
- **HANDOFF.md** -- Fleshed out with real milestones from the implementation guide.
- **README.md** -- Revisited to add core concepts and implementation phases.

After Phase 2, `INIT-GUIDE.md` is deleted -- the project is fully initialized.

### Phase 3 -- Ongoing Development

As you build:

- **TESTING-GUIDE.md** -- Filled in when the first tests are written.
- **Session logs** -- The agent creates a log in `logs/` at the end of each session, following the format in `logs/SESSION-LOG-TEMPLATE.md`. Each log is saved as `logs/YYYY-MM-DD-session-NN-slug.md`. The last 5 are linked from HANDOFF.md; older ones are moved to HANDOFF-ARCHIVE.md.
- **HANDOFF.md** -- Updated every session with current status and next actions.

## Session Continuity

Every session starts the same way: the agent reads `AGENT-warm-up.md`. This is the only file the agent needs to be pointed to -- it serves as the bootstrap for every session, whether it's the first or the fiftieth.

1. **Agent reads `AGENT-warm-up.md`** -- gets the project title, codebase location, and workflow instructions.
2. **First session:** `AGENT-warm-up.md` detects `INIT-GUIDE.md` and triggers the initialization process.
3. **Later sessions:** The agent follows links to `README.md` for overview and `HANDOFF.md` for current status, next actions, and session history.
4. `HANDOFF.md` links to session logs and all other documents as needed.

The handoff quality test: *"Could a new team member read HANDOFF.md and implement the next phase without asking clarifying questions?"*

## Document Roles at a Glance

| Document | Role | When Filled |
|----------|------|-------------|
| **SPEC.md** | What to build and why | Phase 1 |
| **DESIGN.md** | How to build it (architecture) | Phase 2 |
| **IMPLEMENTATION-GUIDE.md** | Code-level how-to and phases | Phase 2 |
| **README.md** | Entry point and overview | Phase 1, revised Phase 2 |
| **AGENT-warm-up.md** | Agent context for session start | Phase 1 |
| **HANDOFF.md** | Current status and handoff package | Phase 1 (minimal), then every session |
| **TESTING-GUIDE.md** | How to verify correctness | Phase 3 |
| **INIT-GUIDE.md** | Initialization instructions | Deleted after Phase 2 |

## Suggested Methodology

### Discuss First, Code Later

The template enforces a deliberate progression: **spec -> design -> implement**. Before any code is written, talk through the problem, the approach, and the trade-offs with the agent. This conversation is where misunderstandings surface, scope gets clarified, and bad ideas get caught cheaply. Jumping straight to code skips the cheapest opportunity to course-correct -- reworking a paragraph in SPEC.md costs nothing compared to reworking an implementation.

### Describe the Problem, Let the Agent Draft

You don't need to write the spec yourself. Describe what you want to solve or the idea you have in mind, and let the agent research, propose a solution, and draft the spec. Your job is to review what the agent produces -- adjust scope, correct misunderstandings, add constraints the agent missed, and remove things that don't fit. This review-and-adjust cycle is where the real value lies. The agent does the heavy lifting of structuring the spec; you provide the domain knowledge and judgment.

### Ask, Don't Tell

Even when you already have a solution in mind, don't hand it to the agent directly. Instead, describe the problem and ask the agent to propose a solution. Then review and adjust what it comes back with. This serves as a comprehension check -- if the agent proposes something close to what you had in mind, you know it understands the problem. If it proposes something different, either it caught something you missed, or its understanding is off and you can correct it before that misunderstanding propagates into the spec, design, and code.

### Keep Documents Honest

Documents should reflect reality, not aspirations. When implementation reveals that a design decision was wrong, update DESIGN.md *before* changing the code. When a requirement turns out to be infeasible, update SPEC.md. The documents are only useful as long as they match the actual state of the project. The agent is instructed to do this, but you should hold it to that standard.

### One Session, One Focus

Each session should have a clear goal: "draft the spec," "design the data model," "implement Phase 1 milestone 2." Trying to do everything in one session leads to shallow work across many documents rather than thorough work on one thing. The session log and HANDOFF.md updates at the end of each session make it cheap to pick up exactly where you left off.

### Review the Handoff

At the end of each session, read the HANDOFF.md update the agent produces. This is your quality gate -- if the status, next actions, or session summary don't accurately capture what happened, correct them immediately. A sloppy handoff compounds across sessions.

### Let the Spec Evolve

The spec is not frozen after Phase 1. As you learn more during design and implementation, go back and update it. Add new constraints you discovered, remove requirements that turned out to be unnecessary, and close open questions. A living spec is far more valuable than a pristine one that no longer reflects the project.

## Tips

- **Start with the spec.** Don't jump to design or code. The agent will guide you through the spec first, and that clarity pays off in every later phase.
- **Use open questions.** If you're unsure about a requirement, put it in the Open Questions section of SPEC.md rather than guessing. Resolve these before moving to design.
- **Keep documents linked.** The template creates a web of interconnected documents. When adding content, link to related sections in other docs.
- **Trust the agent's workflow.** The agent knows the initialization sequence. Just answer its questions and iterate on the content together.

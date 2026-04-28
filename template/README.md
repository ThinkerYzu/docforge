# {{PROJECT_TITLE}}

**Status:** Phase 1 — {{current status}}
**Created:** {{YYYY-MM-DD}}
**Last Updated:** {{YYYY-MM-DD}}
**Goal:** {{one-sentence goal}}

---

## Project Documentation

### Core Documentation

- **README.md** (This document) - Project overview and getting started
- **[SPEC.md](SPEC.md)** — Problem statement, requirements, constraints, and success criteria
- **[DESIGN.md](DESIGN.md)** — Architecture, design decisions, and technical approach
- **[IMPLEMENTATION-GUIDE.md](IMPLEMENTATION-GUIDE.md)** — Detailed implementation guide with code examples
- **[HANDOFF.md](HANDOFF.md)** — Current status, next actions, session logs (the handoff package)

### Testing Documentation

- **[TESTING-GUIDE.md](TESTING-GUIDE.md)** — Testing procedures, expected output, troubleshooting

**Quick Links:**
- [Overview](#overview) | [Design & Architecture](DESIGN.md) | [Current Status](HANDOFF.md#current-status) | [Testing](TESTING-GUIDE.md)

---

## Overview

{{Describe what this project does, why it exists, and what problem it solves. 2-3 paragraphs.}}

## Recent Updates

See [HANDOFF.md](HANDOFF.md) for the full changelog, session history, and next actions.

---

## Core Concepts

### {{Concept 1}}

{{Explain the fundamental idea.}}

### {{Concept 2}}

{{Explain the fundamental idea.}}

---

## Implementation Phases

### Phase 1: {{Phase Name}} (IN PROGRESS)
- {{milestone 1}}
- {{milestone 2}}

### Phase 2: {{Phase Name}} (FUTURE)
- {{milestone 1}}
- {{milestone 2}}

---

## Development Repository

**Working Directory:** {{path to source code}}
**Git Branch:** {{branch name}}

---

## Related Projects

- {{links to related projects, knowledge base docs, etc.}}

---

## Documentation Maintenance

### Documentation as a Web

**Core Principle:** This project directory is maintained as a **web of interconnected documents**, not isolated files.

- Documents are connected through **hyperlinks** (both markdown and HTML)
- Every document includes **navigation sections** at the top
- Cross-references point to **specific sections** using anchor links (#section-name)

### Agent Responsibilities

The agent (Claude) must actively maintain both **content and connections** in this documentation web:

**Content updates:**
- **Progress tracking**: Update status and milestone achievements
- **Implementation details**: Document design decisions, code structure, and technical approaches
- **Technical findings**: Record measurements, results, and key learnings
- **Architecture evolution**: Update design documents as the design evolves
- **Log maintenance**: Keep HANDOFF.md current with development activities

**Link maintenance:**
- **Add cross-references**: When creating new content, link to related existing content
- **Update navigation**: Add new documents to navigation bars on all pages
- **Verify links**: Ensure links remain valid as documents evolve

### Handoff as Complete Package

**Philosophy:** HANDOFF.md should serve as a **complete handoff package** that enables anyone to pick up the task and push forward without asking questions.

**Handoff quality test:** "Could a new team member read this and implement the next phase without asking clarifying questions?"

---

**Last Updated:** {{YYYY-MM-DD}}

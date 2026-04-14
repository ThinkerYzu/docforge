# Implementation Guide: {{PROJECT_TITLE}}

**Project:** {{PROJECT_TITLE}}
**Created:** {{YYYY-MM-DD}}
**Last Updated:** {{YYYY-MM-DD}}
**Status:** {{phase and completion status}}

---

## Navigation

**Project Docs:** [README](README.md) | [SPEC](SPEC.md) | [DESIGN](DESIGN.md) | [IMPLEMENTATION-GUIDE](IMPLEMENTATION-GUIDE.md) *(you are here)* | [HANDOFF](HANDOFF.md)

**This Document:**
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [File Structure](#file-structure)
- [Implementation Details](#implementation-details)
- [Implementation Phases](#implementation-phases)
- [Build & Test](#build--test)

---

## Overview

### What We're Building

{{Summarize the implementation scope — what does the code do end-to-end?}}

### Key Principle

{{The most important implementation principle, e.g., "Validate Before Replace", "Incremental Delivery"}}

---

## Prerequisites

### Dependencies

- {{dependency 1}} — {{version, why needed}}
- {{dependency 2}} — {{version, why needed}}

### Build Environment

```bash
{{build setup commands}}
```

---

## File Structure

```
{{project-root}}/
  {{file/dir}}    — {{purpose}}
  {{file/dir}}    — {{purpose}}
  {{file/dir}}    — {{purpose}}
```

---

## Implementation Details

### {{Component/Module 1}}

{{Explain the implementation approach. Include code examples where helpful.}}

```{{language}}
{{code example}}
```

**Key points:**
- {{important implementation detail}}
- {{gotcha or non-obvious behavior}}

### {{Component/Module 2}}

{{Explain the implementation approach.}}

---

## Implementation Phases

### Phase 1: {{Phase Name}}

**Goal:** {{what this phase achieves}}
**Status:** {{IN PROGRESS / COMPLETE}}

Steps:
1. {{step description}}
2. {{step description}}

**Validation:** {{how to verify this phase is complete}}

### Phase 2: {{Phase Name}}

**Goal:** {{what this phase achieves}}
**Status:** {{NOT STARTED / IN PROGRESS / COMPLETE}}

Steps:
1. {{step description}}
2. {{step description}}

**Validation:** {{how to verify this phase is complete}}

---

## Build & Test

### Building

```bash
{{build commands}}
```

### Running

```bash
{{run commands}}
```

### Quick Validation

```bash
{{command to verify everything works}}
```

---

**Last Updated:** {{YYYY-MM-DD}}

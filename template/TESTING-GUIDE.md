# Testing Guide: {{PROJECT_TITLE}}

**Scope:** How to run tests, what each test validates, expected output, and troubleshooting.

**Current test count:** {{N}} tests covering {{scope description}}.

---

## Navigation

**Project Docs:** [README](README.md) | [SPEC](SPEC.md) | [DESIGN](DESIGN.md) | [IMPLEMENTATION-GUIDE](IMPLEMENTATION-GUIDE.md) | [HANDOFF](HANDOFF.md)

**This Document:**
- [Quick Start](#quick-start)
- [Test Inventory](#test-inventory)
- [Running Tests](#running-tests)
- [Expected Output](#expected-output)
- [Troubleshooting](#troubleshooting)

---

## Quick Start

```bash
{{single command to run all tests}}
```

Expected final line:

```
{{expected success output}}
```

---

## Test Inventory

### {{Test Category 1}}

| # | Test Name | What It Validates | Pass Criteria |
|---|-----------|-------------------|---------------|
| 1 | {{name}} | {{description}} | {{criteria}} |
| 2 | {{name}} | {{description}} | {{criteria}} |

### {{Test Category 2}}

| # | Test Name | What It Validates | Pass Criteria |
|---|-----------|-------------------|---------------|
| 3 | {{name}} | {{description}} | {{criteria}} |

---

## Running Tests

### Full Test Suite

```bash
{{command}}
```

### Individual Tests

```bash
{{command to run a specific test}}
```

---

## Expected Output

### Successful Run

```
{{example output from a passing test run}}
```

### Known Acceptable Differences

- {{description of expected variations, e.g., floating point tolerance}}

---

## Troubleshooting

### {{Common Problem 1}}

**Symptom:** {{what you see}}
**Cause:** {{why it happens}}
**Fix:** {{how to resolve}}

### {{Common Problem 2}}

**Symptom:** {{what you see}}
**Cause:** {{why it happens}}
**Fix:** {{how to resolve}}

---

**Last Updated:** {{YYYY-MM-DD}}

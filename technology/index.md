---
layout: default
title: Technology
description: Open-source tools built for the Iran Transition Project
---

## Technology

The ITP analytical engine is built on open-source infrastructure. These
tools are developed as part of the project and available independently
for anyone building multi-agent AI workflows.

---

### Heddle

**Actor-based Python framework for orchestrating multi-LLM workflows.**

Heddle splits AI work into focused, testable steps with typed contracts
instead of one monolithic prompt. Workers communicate via NATS messaging,
enabling parallel execution across different model tiers (local Ollama,
Claude Sonnet, Claude Opus).

- 12 CLI commands, Workshop web UI, MCP gateway
- Pipeline orchestration with automatic parallelism
- Knowledge silos and blind audit patterns
- OpenTelemetry distributed tracing

**Links:**
[GitHub](https://github.com/getheddle/heddle) |
[API Documentation](https://getheddle.github.io/heddle/) |
[Issues](https://github.com/getheddle/heddle/issues) |
[Discussions](https://github.com/getheddle/heddle/discussions)

---

### Baft

**ITP analytical engine -- application layer on Heddle.**

Baft provides 13 specialized worker configurations, 3-tier pipeline
orchestration, a blind audit system for publication quality control,
and session management for multi-analyst support.

- 13 workers across local, standard, and frontier model tiers
- Epistemic quarantine: audit workers are deliberately information-deprived
- Typed Pydantic I/O contracts for all workers
- DuckDB analytical database with incremental import from YAML

**Links:**
[GitHub](https://github.com/IranTransitionProject/baft) |
[Issues](https://github.com/IranTransitionProject/baft/issues)

---

### Docman

**Document processing pipeline built on Heddle.**

Extracts content from PDF, DOCX, PPTX, XLSX, and HTML files using
adaptive two-tier extraction (MarkItDown for speed, Docling for depth).
LLM-based classification and summarization with DuckDB persistence
and vector search.

**Links:**
[GitHub](https://github.com/IranTransitionProject/docman) |
[Issues](https://github.com/IranTransitionProject/docman/issues)

---

### Baseline

**ITP analytical database -- YAML source of truth.**

The baseline repository contains all structured analytical data:
22 content modules, 86 tracked variables, 57 research gaps,
12 scenario models, and 14 convergence briefs. Maintained as a
live Git repository with every analytical decision tracked in
commit history.

Validated by JSON Schema on every commit. Built into PDF releases
via Jinja2 templates.

**Links:**
[GitHub](https://github.com/IranTransitionProject/baseline) |
[Discussions](https://github.com/IranTransitionProject/baseline/discussions) |
[Releases (PDF)](https://github.com/IranTransitionProject/baseline/releases)

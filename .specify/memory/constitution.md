<!--
SYNC IMPACT REPORT
- Version change: 1.0.0 -> 1.1.0
- List of modified principles:
  - I. Clarity & Completeness -> Upgraded to I. Clarity & Collaborative Ambiguity Resolution (mandating relentless user interviewing and collaborative shaping).
  - III. Precise & Formal Contracts -> Upgraded to III. Ordered Gherkin-Style Specifications & Tasks (mandating ordered tasks grouped by feature and complete Given/When/Then acceptance criteria).
  - IV. Independent Test Slices -> Upgraded to IV. Strict Test-First Mindset & TDD (mandating non-negotiable Test-Driven Development before functional implementation).
- Added sections: None
- Removed sections: None
- Templates requiring updates:
  - .specify/templates/spec-template.md (✅ aligned)
  - .specify/templates/plan-template.md (✅ aligned)
  - .specify/templates/tasks-template.md (✅ aligned)
- Follow-up TODOs: None
-->

# Solutioning Constitution

This constitution establishes the governing principles, design standards, and workflows for writing, reviewing, and managing Software Design Document (SDD) specifications within the `solutioning` repository. Compliance with these principles is mandatory and non-negotiable.

---

## Core Principles

### I. Clarity & Collaborative Ambiguity Resolution (No Guesswork)
Every Software Design Document (SDD) MUST be self-contained, clear, and completely free of ambiguity.
- **Collaborative Requirements Shaping**: The development process begins with a high-level description provided by the user. The AI agent MUST actively collaborate to shape and refine these into robust requirements.
- **Relentless Interviewing**: During the planning phase, the agent MUST continuously review the proposed plan and relentlessly interview the user with structured questions to identify and resolve every potential ambiguity before starting implementation.

### II. Spec-Driven Governance (Spec Before Code)
No implementation code changes or task execution can begin until a formal specification has been written, reviewed, and ratified. The specification serves as the absolute "source of truth" for the codebase. Specifying is the primary mode of alignment.

### III. Ordered Gherkin-Style Specifications & Tasks
Requirements and specifications MUST be written in highly precise language.
- **Ordered Task Decompositions**: Requirements must evolve into a strictly ordered set of tasks, logically grouped by feature.
- **Gherkin-Style Acceptance Criteria**: Features and tasks MUST be defined by complete sets of acceptance criteria written in the formal Gherkin style:
  ```gherkin
  Given [initial context or state]
  When [an event or action occurs]
  Then [the expected outcome or state change is verified]
  ```
- **Explicit Contracts**: All API endpoints, payloads, and database schemas MUST be defined with explicit types (e.g., OpenAPI, JSON Schema) alongside success and failure test mocks.

### IV. Strict Test-First Mindset & TDD (Non-Negotiable)
All software solutions MUST be designed and developed with a strict test-first mindset.
- **TDD Mandate**: Test-Driven Development (TDD) is an absolute, non-negotiable implementation requirement. Tests MUST be written and verified as failing (or fully stubbed) before any functional production code is created.
- **Independent Test Slices**: Features MUST be partitioned into prioritized, independently testable user journeys (P1, P2, P3). Slices must deliver independent value and be verifiable in isolation.

### V. Architectural Decision Transparency (ADRs)
Significant architectural choices, trade-offs, and technology evaluations MUST be documented as Architecture Decision Records (ADRs). Each ADR must explain the context, options considered, the final decision, and the resulting consequences.

---

## Technical & Documentation Standards

### Markdown & Visuals
- All specifications and documentation MUST use standard GitHub Flavored Markdown (GFM).
- All system architectures, workflows, and data flows MUST be illustrated using `mermaid` diagram blocks to ensure version control friendliness.
- Vague language (e.g., "the system should perform well") MUST be replaced with concrete, measurable limits (e.g., "latency MUST be under 200ms at p95").
- No placeholders or "TODOs" are permitted in ratified specifications. Every requirement must be fully resolved.

---

## Development & Review Workflow

### 1. Specification Stage
Draft the SDD in a feature branch matching `specs/<domain>/[###-feature-name]`. Establish initial requirements and align on schemas and boundaries using `/speckit.specify`.

### 2. Planning & Tasks Stage
Generate the implementation plan (`plan.md`) and the task checklist (`tasks.md`) based on the spec. Ensure tasks represent complete, Gherkin-compliant units of work matching the P1/P2/P3 priority slices.

### 3. Peer Review & Ratification
Open a Pull Request (PR) to merge the spec/plan/tasks into `main`. The PR must satisfy the SDD verification list (completeness, security, compliance, testability). Merging to `main` officially ratifies the specification.

---

## Governance

### Amendments & Versioning
- This Constitution supersedes all other codebase practices.
- Amendments to this Constitution or core templates require an approved PR and a version bump:
  - **MAJOR**: Changes that modify or remove core principles or non-negotiable standards.
  - **MINOR**: Additions of new principles, sections, or materially expanded workflow guidelines.
  - **PATCH**: Typo corrections, non-semantic wording updates, and template formatting tweaks.

**Version**: 1.1.0 | **Ratified**: 2026-05-20 | **Last Amended**: 2026-05-20


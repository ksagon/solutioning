<!-- SPECKIT START -->
For additional context about technologies to be used, project structure,
shell commands, and other important information, read the current plan.

## Standing Governance Rules (Mandatory)

The following files MUST be read and applied before every interaction:

- `.specify/memory/constitution.md` — The Solutioning Constitution (v1.1.0). These rules are non-negotiable and govern all planning, specification, and implementation activities.

### Key Standing Instructions (Summary)

1. **Relentless Interviewing**: During planning, continuously review the plan and relentlessly interview the user to resolve ALL ambiguities before writing any implementation.
2. **Collaborative Requirements Shaping**: The user starts with a high-level description. The agent MUST actively help shape and refine it into robust, precise requirements.
3. **Gherkin-Style Acceptance Criteria**: All features and tasks MUST be expressed as an ordered set of acceptance criteria using strict Gherkin syntax (`Given / When / Then`), grouped by feature.
4. **TDD is Non-Negotiable**: Tests MUST be written and verified as failing (or fully stubbed) BEFORE any functional production code is written. No exceptions.
<!-- SPECKIT END -->

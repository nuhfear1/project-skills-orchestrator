# Orchestration Policy

## 1. Source of truth

This GitHub repository is the canonical source for the orchestrator. Updates are made by commits in this repository. ZIP archives are milestone exports only.

## 2. Resource types

- **Skill:** agent instructions with a real `SKILL.md`.
- **Library:** project dependency installed through its official package manager.
- **Tool:** external service, CLI, MCP server, registry or platform.

Never reclassify a library or tool as a skill without a real audited skill package.

## 3. Default state

New resources are disabled by default until audited and selected for a project.

## 4. Preservation

Preserve approved upstream skills intact. Apply corrections and restrictions from the external registry and audit files. Fork only when necessary.

## 5. Authority

A resource may only decide within its declared authority. Design resources do not decide product strategy. Animation resources do not select the 3D engine. Component registries do not define the final visual direction.

## 6. Project scope

Libraries and tools are installed only in the repository or cloud environment of the project that selected them. Never attach project-specific tooling to an unrelated repository.

## 7. Approval gates

- `DISCOVERY_NOT_VALIDATED`
- `ARCHITECTURE_NOT_VALIDATED`
- `DESIGN_NOT_VALIDATED`
- `IMPLEMENTATION_NOT_AUTHORIZED`
- `IMPLEMENTATION_IN_PROGRESS`
- `REVIEW_REQUIRED`
- `APPROVED`

No implementation, publishing or deployment may occur before the appropriate explicit approval.

## 8. External tools

Research and read-only consultation may occur when allowed. Writes, installations, publishing, code generation into external projects and destructive actions require explicit approval.

## 9. Secrets

Never store API keys, tokens, passwords or production secrets in this repository. Store them in the target project's environment variables or secret manager.

## 10. Conflicts

When two resources overlap, assign a single owner for each state, property, animation, data source or architectural decision. Avoid shared ownership without an explicit integration rule.

## 11. Versioning

An audit applies to the exact reviewed version or commit. New major versions require review. Security-sensitive or behavior-changing updates require re-audit even without a major version bump.

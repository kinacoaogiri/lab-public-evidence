# CONSOLE Context/Prompt Compiler (CCPC) — Canonical Requirements

Date: 2026-09-10
Status: REQUIREMENTS / ARCHITECTURE DECISION

## 1. Scope

CCPC compiles one Human Intent / Mission and its relevant Context Sources into execution-ready directive packages while preserving canonical mission semantics, authority boundaries, context lineage, and acceptance requirements.

CCPC is designed as an independently operable product boundary. The first integration target is CONSOLE, but CONSOLE is not a runtime dependency of CCPC Core.

## 2. Product Boundary

Dependency direction:

```text
CCPC Core              <- standalone product / no CONSOLE dependency
   |
   +-- Generation Adapters
   |     +-- text/code agents
   |     +-- target-specific AI systems
   |     +-- non-verbal generation systems
   |
   +-- Organization Adapter
             |
             v
          CONSOLE
```

Hard rule:

- CCPC Core MUST NOT depend on CONSOLE.
- CONSOLE MAY invoke CCPC through an explicit Organization Adapter / contract.
- No CCPC Core API, schema, storage layout, compiler stage, or Core test may assume that CONSOLE is installed or running.

## 3. Standalone Mode

Standalone Mode accepts Human Intent plus available Context Sources such as repository content, documents, rules, project history, and explicit references.

Minimum Agent-ready Package:

- Mission / Task
- Requirements
- Relevant Context
- Constraints
- Acceptance Criteria
- References / lineage
- Output Contract

Standalone Mode does not require CONSOLE Organization, Manager, Control Machine, Race Control, or Mission Scheduler runtime.

## 4. CONSOLE Integration Mode

CONSOLE Integration Mode extends the same canonical mission semantics into a Mission Semantic Model / Organization Contract and coordinated Role-specific Initial Directives.

One Mission source is projected to four organizational responsibilities:

| Department | Role | Initial Directive |
|---|---|---|
| Design | Chief Architect | Design Initiation Directive |
| Development | Senior PM | Mission Execution Directive |
| Quality Assurance | Debugger Leader | QA / Debug Readiness Directive |
| Human Resources / Organization | Orchestration Processor under Orchestration Manager | Organization & Operation Directive |

The four directives MUST be projections of one canonical Mission Semantic Model / Organization Contract, not four independently authored prompts.

Goal, Requirements, Constraints, Acceptance, Authority, Dependencies, Risk, and Context References must remain semantically consistent across projections.

## 5. Compiler Pipeline

```text
Human Intent
    -> Context Acquisition
    -> Mission Semantic Model
    -> Organization Contract (when applicable)
    -> deterministic Role / Target projection
    -> bounded intelligence assistance where necessary
    -> validation
    -> Directive / Agent-ready Packages
    -> compilation Evidence + lineage
```

Target-specific prompt dialect, syntax, transport details, or generation-model constraints must not contaminate the canonical Mission semantics upstream.

## 6. Generation Adapters

Generation Adapters translate canonical CCPC output for specific execution/generation targets.

They may support text/code agents and non-verbal generation systems. The planned non-verbal generation LLM translation layer may be implemented as, or behind, a CCPC Generation Adapter while preserving a model-neutral canonical representation upstream.

Replacing a target adapter must not require rewriting the canonical Human Intent / Mission semantics.

## 7. Escalation Enforcement

Normal escalation remains Role/Manager mediated. Direct Processor-to-Processor escalation is prohibited.

Orchestration Manager is a legitimate bounded bypass/escalation route only when defined eligibility conditions are satisfied.

Required Control-side enforcement:

1. Escalation Eligibility Gate before bypass delivery.
2. Chief Architect Admission Gate before architecture escalation is admitted.
3. Non-architecture escalation is rejected with `REJECT_ESCALATION / RETURN_TO_ROUTING` and returned to the appropriate route.

Minimum escalation object:

- EscalationId
- SourceManagerId
- SourceRole
- MissionId / WPId
- ReasonCode
- AuthorityRequired
- NormalRoute
- BypassRoute
- BypassReason
- AttemptedRemedies[]
- EvidenceRefs[]
- ContextRefs[]
- DecisionRequired
- TargetRole
- CreatedAt

AIME Bridge is transport only. It has no Routing Authority, Control Authority, state-mutation authority, or independent escalation authority.

Repository/folder reading for Chief Architect is Context Acquisition under Manager/authorized read capability. A Processor does not self-grant repository access.

## 8. Orchestration Processor

Orchestration Manager MAY attach an Orchestration Processor when organization-level judgment is required, particularly for multi-Team operation. Attachment is optional rather than universally mandatory.

Responsibilities include recommendations for:

- Team formation
- Processor placement
- Processor replacement / reallocation
- capacity balancing
- Team/Mission startup coordination
- organization-level operational optimization

The Orchestration Processor has no Control Authority. It recommends; Control Machine / Processor Controller performs authoritative state transitions such as ATTACH, DETACH, REPLACE, PARK, and routing changes.

Deterministic policy remains deterministic. Cases already resolved by policy, including Same-Reason Two-Strike Processor Reliability Failure, are not reopened for discretionary AI judgment.

Possible recommendation outcomes include RETAIN, REPLACE, REALLOCATE, PARK, WAIT, and ESCALATE. Execution remains subject to Manager/Control Policy and Authority checks.

## 9. CCPC v1 Hard Acceptance

CCPC v1 must demonstrate:

1. one Human Intent can produce a valid standalone Agent-ready Package without CONSOLE;
2. the same canonical Mission representation can support 1-Agent standalone compilation and N-Role CONSOLE compilation;
3. simultaneous generation of the four CONSOLE Role directives;
4. cross-directive semantic consistency;
5. role/target-minimum relevant Context selection;
6. Authority Boundary preservation;
7. Context / Evidence / Canonical lineage retention;
8. Orchestration Processor remains non-authoritative;
9. escalation remains gated;
10. Processor replacement does not erase persistent Manager/Role context;
11. machine-readable Directive Contracts are produced;
12. compilation Evidence is reproducible;
13. target adapter replacement does not modify canonical Mission semantics.

## 10. Product Positioning Boundary

- **CCPC** determines WHAT context, instructions, constraints, acceptance criteria, references, and contracts should be delivered to an AI execution target.
- **CONSOLE** governs HOW an AI organization is formed, routed, controlled, evidenced, and operated.
- **Dev-Capsule** applies that organizational capability to software-development Missions.

A standalone CCPC Mission can later be promoted into CONSOLE organization execution without rewriting Human Intent from scratch.

## 11. Immediate Implementation Order

1. Implement and verify Escalation Eligibility Gate + Chief Architect Admission Gate.
2. Implement optional Orchestration Processor capability and recommendation contract without granting Control Authority.
3. Freeze CCPC v1 implementation design against current Canonical and Context Builder assets.
4. Implement CCPC Core as CONSOLE-independent.
5. Implement CCPC Organization Adapter for CONSOLE.
6. Use CCPC to launch the four departments for the planned multi-Team development Mission.
7. Apply the resulting organization to the non-verbal generation LLM translation layer before the 2026-09-15 benchmark.

## Claim Boundary

This document records current project requirements and architecture decisions. It does not claim that all requirements described here are already implemented or programmatically ENFORCED. `ENFORCED` is reserved for boundaries demonstrated by implementation and evidence.

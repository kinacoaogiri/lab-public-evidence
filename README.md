# CONSOLE Lab. — Public Evidence

This repository publishes reproducible evidence, benchmark results, and observed implementation outcomes for CONSOLE Lab. products and experiments.

The purpose is deliberately narrower than publishing product specifications or source code: **show what was actually demonstrated, including failures and limitations, without exposing unpublished canonical architecture.**

## Evidence principles

- Observed results are separated from architectural intent and originality claims.
- `PASS`, `BLOCKED`, and `NOT PASS` are all publishable outcomes.
- Failed experiments are retained when they materially define a capability boundary.
- Evidence should state acceptance conditions, observed path, limitations, and relevant measurements.
- Unpublished product canonical, internal requirements, credentials, private paths, personal information, and proprietary implementation details are not public evidence.
- Screenshots are evidence only when they are authentic captures. Generated or reconstructed images are never presented as observed evidence.

## Dev-Capsule

Dev-Capsule explores AI development organizations in which persistent organizational roles can be bound to replaceable AI processors, with explicit routing, authority boundaries, evidence, and failure handling.

### Published

#### Chief Architect Executive Seat — Live E2E — 2026-09-10

**Result:** `PASS`

A human-facing Chief Architect seat inside Visual Studio Code completed a live end-to-end conversation through a persistent Chief Architect Manager to GPT-5.6 Sol in an authenticated ChatGPT Web session and returned the result to the same seat.

Evidence: [`dev-capsule/2026-09-10-chief-architect-executive-seat/`](dev-capsule/2026-09-10-chief-architect-executive-seat/)

### Evidence queue

The following experiments are candidates for publication when their underlying records can be verified and sanitized. Their presence here is **not a PASS claim**.

| Experiment | What it tests | Publication status |
| --- | --- | --- |
| Multi-agent orchestration smoke | Parallel dispatch, independent completion, parent aggregation | Verification / sanitization required |
| Processor replacement | Whether Role / Manager / Mission context survives Processor replacement | Formal evidence required |
| Same-reason two-strike recovery | Detection of repeated failure and replacement rather than blind redispatch | Formal evidence required |
| Single Agent vs Dev-Capsule Team | Wall-clock time, completion quality, total tokens, paid tokens, Human intervention | Controlled benchmark required |
| Free/Default vs TOP Team | Cost/performance trade-off between accessible and high-capability Processor profiles | Field-test-driven benchmark required |
| Team/Raid scaling | Coordination cost and performance as organization size increases | Controlled benchmark required |
| CCPC before/after | Requirement, concern, context, and acceptance coverage from the same Human request | CCPC implementation required |
| OpenCode multi-worker in one VS Code window | Multiple independent workers in VS Code integrated terminals | Current evidence insufficient; publishable as NOT PASS after record verification |

## Benchmark metrics

Where applicable, comparative Dev-Capsule evidence should report more than a single success score. Preferred measurements include:

- acceptance / Done-condition result;
- wall-clock time;
- total token usage;
- paid token usage;
- high-capability Processor token usage;
- Human intervention count;
- redispatch count;
- Processor replacement count; and
- coordination failures or blocked states.

This allows a result such as "more aggregate computation, but less paid-model usage and lower wall-clock time" to be reported without conflating total compute with economic cost.

## Claim boundary

This repository is an evidence ledger, not a declaration that every demonstrated mechanism is novel. Originality claims require separate comparison against prior work.

No source-code release or open-source license grant is implied by publication of evidence in this repository.

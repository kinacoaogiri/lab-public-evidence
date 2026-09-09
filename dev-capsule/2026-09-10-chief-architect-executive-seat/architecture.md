# Architecture Snapshot

Evidence date: 2026-09-10 JST

## Demonstrated boundary

```text
┌─────────────────────────────────────────────┐
│ VS Code                                     │
│                                             │
│  Human-facing Chief Architect Executive Seat│
└──────────────────────┬──────────────────────┘
                       │ Human request / response
                       ▼
              Persistent Manager
              seat-chief-architect
                       │
                       │ Processor request/result
                       ▼
              Replaceable Processor
                 GPT-5.6 Sol
                       │
                       ▼
             ChatGPT Web transport
```

The organizational identity is bound to the persistent Manager seat rather than directly to the Processor. The Processor is therefore an execution/intelligence attachment, not the canonical identity of the Chief Architect Role.

## Separation of concerns

### Executive Seat
Human-facing input, output, and status presentation.

### Manager
Persistent Role identity and the path through which the human request and Processor result pass.

### Processor
Replaceable intelligence provider. During this demonstration the Processor was GPT-5.6 Sol.

### Transport
The demonstrated model interaction used an authenticated ChatGPT Web session rather than the OpenAI API.

## Evidence boundary

The Live E2E demonstration establishes that this path executed successfully for the Chief Architect reference seat. It does not by itself establish novelty of the individual transport techniques or completion of the wider Dev-Capsule / CONSOLE architecture.

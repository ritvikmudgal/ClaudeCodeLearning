##  CLAUDE ARCHITECTURE STACK
```
            ┌──────────────────────────────────────────┐
            │               USER INPUT                 │
            └──────────────────────────────────────────┘
                              │
                              ▼
            ┌──────────────────────────────────────────┐
            │        APPLICATION / PRODUCT LAYER        │
            │   (Claude desktop, web, API, integrations)│
            └──────────────────────────────────────────┘
                              │
                              ▼
            ┌──────────────────────────────────────────┐
            │        ORCHESTRATION & SAFETY LAYER      │
            │ - Prompt routing / formatting            │
            │ - Context building                       │
            │ - Tool calling / API wrappers            │
            │ - Safety filters / policy enforcement    │
            └──────────────────────────────────────────┘
                              │
                              ▼
            ┌──────────────────────────────────────────┐
            │        MODEL INFERENCE LAYER             │
            │ - Claude model execution                 │
            │ - Distributed inference engines          │
            │ - Quantization / batching                │
            └──────────────────────────────────────────┘
                              │
                              ▼
            ┌──────────────────────────────────────────┐
            │       TRAINED FOUNDATION MODEL (LLM)     │
            │ - Weights (parameters)                   │
            │ - Token embeddings                       │
            │ - Attention + MLP blocks                 │
            │ - Positional encodings                   │
            └──────────────────────────────────────────┘
                              │
                              ▼
            ┌──────────────────────────────────────────┐
            │        TRAINING DATA + PIPELINES         │
            │ - Curated datasets                       │
            │ - RLHF / preference optimization         │
            │ - Safety tuning                          │
            └──────────────────────────────────────────┘
                              │
                              ▼
            ┌──────────────────────────────────────────┐
            │          HARDWARE INFRASTRUCTURE         │
            │ - GPU clusters (H100/A100)               │
            │ - Distributed compute / networking       │
            │ - Storage (datasets + checkpoints)       │
            └──────────────────────────────────────────┘
```
## AGENT ORCHESTRATION DIAGRAM
```
           ┌───────────────────────────────────────────┐
           │                 USER QUERY                │
           └───────────────────────────────────────────┘
                             │
                             ▼
           ┌───────────────────────────────────────────┐
           │            COORDINATOR AGENT              │
           │  - Understand task                        │
           │  - Decompose problem                      │
           │  - Route to specialists                   │
           │  - Aggregate results                      │
           └───────────────────────────────────────────┘
          /                 |                      \
         /                  |                       \
        ▼                   ▼                        ▼
┌────────────────┐ ┌───────────────────┐ ┌───────────────────┐
│ SPECIALIST A   │ │ SPECIALIST B      │ │ SPECIALIST C      │
│ (Research)     │ │ (Reasoning/Code)  │ │ (Writing/Format)  │
│ - Search        │ │ - Generate logic  │ │ - Structure output│
│ - Summarize     │ │ - Validate steps  │ │ - Final form      │
└────────────────┘ └───────────────────┘ └───────────────────┘
        \                   |                        /
         \                  |                       /
          \                 |                      /
                             ▼
           ┌───────────────────────────────────────────┐
           │         COORDINATOR AGENT (MERGE)         │
           │ - Validate partial outputs                │
           │ - Resolve conflicts                       │
           │ - Produce final answer                    │
           └───────────────────────────────────────────┘
                             │
                             ▼
           ┌───────────────────────────────────────────┐
           │                FINAL OUTPUT                │
           └───────────────────────────────────────────┘
```

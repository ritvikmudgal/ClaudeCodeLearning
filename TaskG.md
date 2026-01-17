# Task G — Multi-Agent Orchestration (Advanced)

## Overview
This task presents a **multi-agent orchestration architecture** in which a central **Coordinator Agent** manages multiple **Specialist Agents** to complete complex requests. The design focuses on clear message flow, deterministic routing, conflict resolution, and structured output merging.

---

## Agents in the System

### 1. Coordinator Agent
**Purpose:** Central controller and orchestrator

**Responsibilities:**
- Interpret user intent
- Maintain workflow state
- Route tasks to specialist agents
- Resolve disagreements between agents
- Merge and return the final output

---

### 2. Planner Agent
**Purpose:** Task decomposition

**Responsibilities:**
- Break down complex requests into smaller steps
- Identify dependencies between tasks
- Define execution order

---

### 3. Research Agent
**Purpose:** Information gathering

**Responsibilities:**
- Collect factual or domain-specific information
- Provide evidence-backed data
- Reduce uncertainty in later stages

---

### 4. Writer Agent
**Purpose:** Content generation

**Responsibilities:**
- Convert structured inputs into human-readable text
- Organize content into clear sections
- Ensure readability and coherence

---

### 5. Verifier Agent
**Purpose:** Validation and quality control

**Responsibilities:**
- Check outputs for correctness and completeness
- Identify contradictions or logical errors
- Ensure alignment with original user intent

---

## Message Flow Diagram

```mermaid
flowchart TD
    User --> Coordinator

    Coordinator --> Planner
    Planner --> Coordinator

    Coordinator --> Researcher
    Researcher --> Coordinator

    Coordinator --> Writer
    Writer --> Coordinator

    Coordinator --> Verifier
    Verifier --> Coordinator

    Coordinator --> User
````

## Routing Policy

The Coordinator Agent routes tasks to specialist agents using a simple rule-based policy:

| Request Type | Routed Agent |
|-------------|--------------|
| Task planning or decomposition | Planner Agent |
| Information lookup or research | Research Agent |
| Text generation or summarization | Writer Agent |
| Output validation and consistency checking | Verifier Agent |

### Routing Rules
- If the request includes **“plan”, “steps”, “break down”** → Planner Agent  
- If the request includes **“research”, “find”, “facts”** → Research Agent  
- If the request includes **“write”, “summarize”, “explain”** → Writer Agent  
- Before final output delivery → Verifier Agent  

---

## Conflict Resolution Strategy

If multiple agents produce conflicting outputs, the Coordinator Agent resolves conflicts using the following priority order:

1. **Verifier Agent** — correctness and logical consistency
2. **Research Agent** — factual accuracy
3. **Planner Agent** — alignment with original task intent
4. **Writer Agent** — style and presentation

If conflicts remain unresolved, the Coordinator re-invokes the relevant agent with clarified instructions.

---

## Final Merge Strategy

The Coordinator Agent merges outputs using the following steps:

1. Collect outputs from all specialist agents
2. Normalize formatting and terminology
3. Resolve conflicts using the defined priority rules
4. Integrate outputs into a single coherent response
5. Perform a final validation check
6. Return the merged result to the user

---

## Example Workflow Execution Trace 

1. User submits a complex multi-part request
2. Coordinator analyzes intent and scope
3. Planner Agent decomposes the task
4. Research Agent gathers supporting information
5. Writer Agent generates structured content
6. Verifier Agent validates correctness and completeness
7. Coordinator merges outputs and returns the final response

---

## Conclusion

This multi-agent orchestration design demonstrates how centralized coordination combined with specialized agents enables reliable handling of complex workflows. Routing, conflict resolution, and structured merging ensure high-quality, consistent outputs.

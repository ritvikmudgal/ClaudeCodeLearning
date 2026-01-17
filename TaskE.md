# Agent Definition

An **agent** is a specialized autonomous role that:

- Has a mission  
- Operates under policies  
- Has tool permissions  
- Manages memory  
- Produces testable outputs  

---

## Agent Structure

Every agent defines the following aspects:

| Aspect | Meaning |
|------|--------|
| Role & Mission | Why the agent exists |
| Scope | What it must avoid |
| Tool Permissions | Which tools it may call |
| Guardrails | Safety constraints |
| I/O Contract | What it accepts and returns |
| Memory Strategy | What persists or resets |
| Evaluation | How its success is scored |

---

## Agent Patterns

### 1. Single-Agent Pattern
One agent handles **planning**, **execution**, and **tooling**.

**Use cases:**
- Small tasks  
- Automation scripts  

---

### 2. Multi-Agent Pattern
A coordinator agent delegates work to specialists:

- **Planner** → decomposes tasks  
- **Researcher** → gathers data  
- **Writer** → generates text  
- **Verifier** → checks outputs  

**Use cases:**
- Complex pipelines  
- Documentation  
- Reports  

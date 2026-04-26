# Claude Architecture Patterns Study Guide

##Not official exam material.
Community study notes compiled from resources and candidate feedback.

If short on time:
1. MCP
2. Multi-agent patterns
3. Reliability / evaluation architecture

## Layered Framework
Study everything through four layers:

1. Prompting — make one model reliable  
2. Agents — make models act  
3. Orchestration — make multiple agents collaborate  
4. Context Infrastructure — make it production grade

---

# Module 1: Prompt Engineering Foundations

## Goal
Master Claude’s reasoning control patterns.

## Study Resources
- Anthropic Prompt Engineering Guide  
https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering

- Prompt Design and Engineering paper  
https://arxiv.org/abs/2401.14423

- Constitutional AI paper  
https://arxiv.org/abs/2212.08073

Topics:
- Constitutional prompting  
- Few-shot prompting  
- Chain-of-thought and reflection loops  
- Structured output prompting  
- XML prompt structuring

## Pattern: Prompt Template
```text
Role
Task
Constraints
Output format
Examples
Evaluation criteria
```

Practice:
- Write 10 reusable system prompts  
- Turn ad hoc prompts into a reusable prompt library

## Pattern: Self-Reflection
```text
Draft
Critique
Revise
Final
```

Build:
- Self-review code assistant  
- Critique chain for business recommendations

Deliverables:
- Prompt pattern cookbook  
- Prompt evaluation scorecard

---

# Module 2: Core Claude Agent Patterns

## Study Resources
- Building Effective Agents  
https://www.anthropic.com/engineering/building-effective-agents

- ReAct paper  
https://arxiv.org/abs/2210.03629

- LangGraph Multi-Agent Workflows  
https://blog.langchain.dev/langgraph-multi-agent-workflows/

## ReAct Pattern
```text
Think
Use tool
Observe
Think
Respond
```

## Planner / Executor Pattern
```text
User
↓
Planner Agent
↓
Executor Agent
↓
Results
```

## Router Pattern
```text
Support Request
→ Billing Agent
→ Technical Agent
→ Escalation Agent
```

Deliverable:
Implement all three patterns.

---

# Module 3: Multi-Agent Architecture

## Study Resources
- Multi-Agent Debate  
https://arxiv.org/abs/2305.14325

- AutoGen  
https://arxiv.org/abs/2308.08155

- CrewAI Docs  
https://docs.crewai.com

## Supervisor Pattern
```text
Supervisor
├── Research Agent
├── Coding Agent
└── QA Agent
```

## Blackboard Pattern
Shared scratchpad for:
- Findings  
- Task state  
- Evidence

## Hierarchical Agent Pattern
```text
Director
 Manager
   Workers
```

## Debate Pattern
Use for:
- Validation  
- Safety  
- Reasoning robustness

Build:
Coordinator + Researcher + Critic + Synthesizer

---

# Module 4: Context Engineering and MCP

## Study Resources
- MCP Documentation  
https://modelcontextprotocol.io

- MCP GitHub  
https://github.com/modelcontextprotocol

- Context Engineering paper  
https://arxiv.org/abs/2603.09619

## Tool Abstraction Pattern
```text
Agent
→ Tool Interface
→ MCP Server
→ System
```

## Retrieval + Agent Pattern
```text
Retrieve
Reason
Act
Verify
```

Study:
- Context packing  
- Relevance ranking  
- Memory compaction  
- Long horizon task state

Build:
- Simple MCP server  
- GitHub or Postgres connector

---

# Module 5: Claude Code Patterns

## Study Resources
- Claude Code Docs  
https://docs.anthropic.com/en/docs/claude-code

- Claude.md research paper  
https://arxiv.org/abs/2509.14744

Patterns:
- Spec → Implement → Review  
- Coding + Critic pair  
- Test generation agents

Build:
Autonomous coding workflow.

---

# Module 6: Production Architecture Patterns

## Study Resources
- OpenAI Evals  
https://github.com/openai/evals

- LangSmith  
https://docs.smith.langchain.com

- Production Grade Agentic Workflows  
https://arxiv.org/abs/2512.08769

Study:
## Reliability Patterns
- Retry loops  
- Guardrails  
- Fallback agents  
- Tool error recovery

## Evaluation Patterns
Build harnesses for:
- Hallucination  
- Task success  
- Tool correctness  
- Latency  
- Cost

## Observability
Track:
- Traces  
- Agent decisions  
- Prompt versions  
- Tool calls

---

# Module 7: Security and Failure Modes

## Study Resources
- OWASP LLM Top 10  
https://owasp.org/www-project-top-10-for-large-language-model-applications/

- NVIDIA Prompt Injection Guide  
https://developer.nvidia.com/blog/securing-llm-systems-against-prompt-injection/

Study:
- Prompt injection  
- Tool poisoning  
- MCP trust boundaries  
- Permission minimization  
- Sandboxed tools

---

# Core Reading Stack

## Must Read
1. Anthropic Prompt Engineering Docs  
2. Building Effective Agents  
3. MCP Documentation  
4. Claude Architect Domains  
5. Claude Code Docs

## Deeper Reading
- Prompt Design and Engineering  
- Production Grade Agentic Workflows  
- Context Engineering  
- ReAct  
- AutoGen

---

# Capstone Project
Build one system with:
- Router agent  
- Planner/executor  
- MCP tool integration  
- Shared memory  
- Evaluation harness  
- Failure handling

---

# 20-Hour Compression Path
Focus on:
1. ReAct  
2. Planner/Executor  
3. Router  
4. Supervisor Pattern  
5. MCP fundamentals  
6. Context engineering  
7. Evaluation harnesses

---

# Architect Mental Model

| Layer | Master |
|---|---|
| Prompting | Single model reliability |
| Agents | Task execution patterns |
| Orchestration | Multi-agent systems |
| Context | MCP + memory |
| Production | Reliability + observability |

---

## High-Value Topics to Over-Index On
- MCP  
- Multi-agent coordination  
- Context engineering  
- Evaluation architecture

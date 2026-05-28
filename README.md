# AgentForge
### Autonomous Multi-Agent AI Workflow Platform built with LangGraph

AgentForge is a stateful multi-agent AI orchestration platform built using LangGraph, Gemini, Playwright, and Gradio.

The platform enables autonomous AI agents to:
- reason through multi-step workflows
- use tools dynamically
- browse and interact with websites
- execute Python code
- persist conversational memory
- self-evaluate responses
- iteratively improve outputs through evaluator feedback loops

This project was designed to explore production-style agentic AI systems and advanced LLM orchestration patterns used in modern AI engineering workflows.

---

# Features

## Multi-Agent Workflow Orchestration
- Built using LangGraph state machines
- Worker–Evaluator agent architecture
- Conditional graph routing between agents and tools
- Stateful execution with persistent memory

## Tool Calling Agents
Agents can autonomously:
- perform web searches
- browse websites using Playwright
- execute Python code
- manage files
- retrieve Wikipedia information
- send push notifications

## Evaluator Feedback Loops
Implemented iterative self-correction workflows where:
- a worker agent generates responses
- an evaluator agent assesses output quality
- feedback is injected back into the workflow
- the worker retries until success criteria are satisfied

This significantly improves:
- response quality
- reasoning consistency
- hallucination reduction

## Persistent Memory & Checkpointing
- LangGraph checkpoint persistence
- SQLite-based conversational memory
- Stateful workflow recovery
- Long-running workflow continuity

## Browser Automation
Integrated Playwright browser automation directly into agent workflows, enabling:
- autonomous web navigation
- dynamic information retrieval
- browser-based task execution

## Interactive User Interface
- Built using Gradio
- Supports interactive AI assistant workflows
- Session-isolated multi-user architecture

---

# Architecture

```text
User
  ↓
Worker Agent
  ↓
Tool Router
  ├── Browser Tools (Playwright)
  ├── Python REPL
  ├── Web Search
  ├── File System Tools
  └── Wikipedia
  ↓
Evaluator Agent
  ↓
Feedback Loop
  ↓
Final Response

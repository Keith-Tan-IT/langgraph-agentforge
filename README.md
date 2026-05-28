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

```

## Tech Stack

### AI / Agent Frameworks
- LangGraph
- LangChain
- Google Gemini API

### Tooling & Automation
- Playwright
- Python REPL
- Google Serper Search API

### Frontend
- Gradio

### State & Persistence
- LangGraph MemorySaver
- SQLite Checkpointing

### Language
- Python

---

## Key Engineering Concepts Demonstrated

- Multi-agent orchestration
- Stateful workflow systems
- Tool calling architectures
- Human-in-the-loop workflows
- Evaluator-worker agent patterns
- Structured outputs
- Persistent conversational memory
- Browser automation agents
- Async programming
- Graph-based AI execution
- Autonomous task execution

---

## Example Use Cases

- Autonomous research assistant
- Browser automation agent
- AI operations co-pilot
- Workflow orchestration engine
- Task automation assistant
- Self-correcting AI systems

---

## Project Structure

```bash
.
├── app.py
├── sidekick.py
├── sidekick_tools.py
├── requirements.txt
└── README.md
```

---

## Running the Project

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Install Playwright Browsers

```bash
playwright install
```

### 3. Configure Environment Variables

Create a `.env` file:

```env
GOOGLE_API_KEY=your_api_key
SERPER_API_KEY=your_api_key
PUSHOVER_TOKEN=your_token
PUSHOVER_USER=your_user
```

### 4. Run the Application

```bash
python app.py
```

---

## Future Improvements

- Vector database memory integration
- Multi-agent collaboration
- RAG pipelines
- Docker deployment
- Cloud deployment
- Observability & tracing
- Authentication & RBAC
- Sandboxed code execution
- Streaming responses
- Multi-modal agents

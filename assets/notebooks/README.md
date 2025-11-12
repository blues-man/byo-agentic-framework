# Agentic Framework Notebooks

This directory contains **4 notebooks** demonstrating different approaches to building AI agents with **Llama Stack** and popular frameworks.

## Two Approaches to Building Agents

### Build with Llama Stack and Red Hat AI

The most streamlined and natively supported path — **full flexibility without framework lock-in**

### BYO Agent Framework

Transparent **integration with your own agent framework**, while using Llama Stack APIs for inference, safety, or evaluation (CrewAI, LangChain/LangGraph, Haystack, etc.)

---

## Notebooks Overview

### 1. [Llama Stack Agent with Responses API](1-llama-stack-agent-responses.ipynb)

**Pure Llama Stack primitives — no frameworks**

Build agents using Llama Stack's native **Responses API** for tool calling with **MCP (Model Context Protocol)** integration.

**What you'll learn:**
- Use Llama Stack's native agentic capabilities
- Integrate server-side MCP tools (Weather, Kubernetes)
- Execute tool calls with automatic function discovery
- Build agents without framework dependencies

**Architecture:**
```
LlamaStackClient → Responses API → MCP Server (Weather/K8s)
```

**Key Features:**
- ✅ Server-side MCP tool execution
- ✅ Automatic tool discovery and routing
- ✅ Native Llama Stack integration
- ✅ Zero framework dependencies

---

### 2. [Llama Stack Agent with RAG](1.1-llama-stack-agent-rag-responses.ipynb)

**Retrieval-Augmented Generation with Llama Stack primitives**

Build a RAG system using **pure Llama Stack APIs** for document retrieval and generation.

**What you'll learn:**
- Create vector stores with PDF documents
- Perform semantic search on embeddings
- Build context-aware responses
- Implement the agentic RAG loop

**Architecture:**
```
User Query → Vector Search → Context Extraction → Responses API → Answer
```

**Key Features:**
- ✅ PDF document ingestion
- ✅ Vector store creation with embeddings
- ✅ Semantic search on financial reports
- ✅ Context-aware response generation

**Example Use Case:**
Query earnings reports for financial metrics, customer information, and operational data.

---

### 3. [LangChain v1.0 with MCP Integration](2-langchain-v1-mcp-agent.ipynb)

**LangChain 1.0 agents with client-side MCP adapters**

Integrate **LangChain** with Llama Stack using the new **MCP adapters** for client-side tool execution.

**What you'll learn:**
- Use LangChain 1.0's `create_agent` API
- Integrate MCP tools with LangChain agents
- Connect to Llama Stack via OpenAI-compatible endpoint
- Execute tools client-side using MCP adapters

**Architecture:**
```
LangChain Agent → ChatOpenAI → Llama Stack Responses API
                ↓
        MCP Client (SSE) → MCP Server (Weather)
```

**Key Features:**
- ✅ LangChain 1.0 agent orchestration
- ✅ Client-side MCP tool execution
- ✅ OpenAI-compatible LLM integration
- ✅ Async agent invocation

---

### 4. [CrewAI Multi-Agent RAG System](3-crewai-mcp-agent.ipynb)

**Multi-agent orchestration with CrewAI and Llama Stack**

Build a **multi-agent RAG system** using CrewAI for orchestration and Llama Stack for inference.

**What you'll learn:**
- Create CrewAI agents with custom tools
- Build RAG tools using Llama Stack Vector Store API
- Orchestrate tasks with CrewAI's Crew framework
- Integrate Llama Stack via OpenAI-compatible endpoint

**Architecture:**
```
CrewAI Agent → Custom RAG Tool → Llama Stack Vector Store API
             ↓
      LLM (via OpenAI endpoint) → Llama Stack Responses API
```

**Key Features:**
- ✅ Custom CrewAI RAG tool
- ✅ Vector store integration
- ✅ Task-based agent orchestration
- ✅ Multi-step reasoning workflows

**Example Use Case:**
Answer customer service questions using a knowledge base of company policies.
# LLM Production Engineering

Production-grade repository for building, optimizing, and deploying Large Language Model (LLM) applications, Retrieval-Augmented Generation (RAG) pipelines, and autonomous AI agent systems.

---

## Overview

This repository provides a structured learning and development environment for modern AI engineering workflows, including:

- Prompt Engineering
- Structured Outputs & JSON Schemas
- Local LLM Deployment with Ollama
- Retrieval-Augmented Generation (RAG)
- Hugging Face Transformers
- Autonomous AI Agents
- Model Fine-Tuning (QLoRA)
- Production Deployment Patterns

---

## Environment Setup

Project dependencies, virtual environments, package management, and lockfile configuration are documented in:

**Setup Guide**

```text
setup/SETUP-new.md
```

---

## Local Model Infrastructure (Ollama)

To improve privacy, reduce API costs, and minimize latency, local open-source models can be used through Ollama.

### 1. Install Ollama

Download and install Ollama from:

https://ollama.com

### 2. Run the Default Local Model

```bash
ollama run llama3.2
```

### Low-Resource Systems

For systems with limited RAM or VRAM:

```bash
ollama run llama3.2:1b
```

> Avoid running large models (e.g., 70B+) on consumer-grade hardware unless sufficient resources are available.

### 3. Troubleshooting

If requests fail because the Ollama service is not running:

```bash
ollama serve
```

### 4. Cloud Fallback

When local hardware becomes a bottleneck, use the provided Google Colab environment:

https://colab.research.google.com/drive/1-_f5XZPsChvfU1sJ0QqCePtIuc55LSdu?usp=sharing

---

## API Configuration & Cost Optimization

This repository is configured around cost-efficient model selection for development and testing.

### OpenAI

Recommended model:

```text
gpt-4o-mini
```

### Anthropic

Recommended model:

```text
claude-3-haiku-20240307
```

### Free Alternatives

Examples using:

- Gemini API
- OpenRouter
- Ollama (Local Models)

are available in:

```text
guides/09_ai_apis_and_ollama.ipynb
```

---

## Usage Monitoring

### OpenAI Dashboard

https://platform.openai.com/usage

### Anthropic Dashboard

https://console.anthropic.com/settings/cost

---

## Core Learning Roadmap

### Prompt Engineering

- System Prompts
- Multi-shot Prompting
- Structured Outputs
- JSON Schemas
- Streaming Responses

### Hugging Face & Transformers

- Transformer Architecture
- Attention Mechanisms
- Tokenization Analysis
- Model Quantization
- PyTorch Workflows

### Retrieval-Augmented Generation (RAG)

- ChromaDB
- FAISS
- Semantic Search
- Embedding Pipelines
- Chunking Strategies
- Re-ranking Techniques
- Evaluation Frameworks

### Autonomous Agents

- Agent Architectures
- Tool Calling
- Workflow Orchestration
- Serverless Execution

### Fine-Tuning

- QLoRA
- PEFT
- Custom Training Pipelines
- Domain Adaptation

---

## Repository Structure

```text
.
├── setup/
├── guides/
├── notebooks/
├── rag/
├── agents/
├── fine_tuning/
├── datasets/
└── README.md
```

---

## License

This project is intended for educational, research, and production engineering workflows. Refer to the repository license for usage details.

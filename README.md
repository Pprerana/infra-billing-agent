# Enterprise AI Billing Investigation Agent

An AI-powered application for investigating infrastructure billing issues across cloud and enterprise environments.

The system allows users to ask natural-language questions about project infrastructure costs, billing rejections, and cost allocation. An AI agent analyzes structured billing and infrastructure data, retrieves relevant organizational policies, and combines the available evidence to explain the root cause of a billing issue and recommend remediation.

The project is inspired by enterprise infrastructure and FinOps workflows, using synthetic data to model the lifecycle from infrastructure planning and resource allocation to billing validation.

## Example

A user asks:

> "Why was Project Alpha's August infrastructure bill rejected?"

The agent can:

1. Identify the relevant project and billing period.
2. Retrieve billing records and actual infrastructure costs.
3. Compare actual usage against approved allocations.
4. Retrieve relevant billing and infrastructure policies using RAG.
5. Determine the likely rejection reason from the available evidence.
6. Explain the finding in natural language.
7. Recommend a remediation action.

## Architecture

```text
React
  ↓
FastAPI
  ↓
AI Agent / Orchestrator
  ├── Billing Data Tool
  ├── Infrastructure Data Tool
  ├── Policy Search / RAG Tool
  └── Cost Analysis Tool
        ↓
 ┌───────────────┬───────────────┐
 │ SQL / Databricks│ Vector Store │
 └───────────────┴───────────────┘
        ↓
     LLM
        ↓
Structured Investigation
        ↓
React UI
```

## Technology

* **Frontend:** React
* **Backend:** Python, FastAPI
* **AI:** LLM APIs, structured outputs, function/tool calling
* **RAG:** Embeddings, vector search
* **Data:** SQL, synthetic billing and infrastructure datasets
* **Analytics:** Databricks
* **Infrastructure:** AWS, Docker
* **Evaluation:** Custom evaluation dataset and automated checks

## Engineering Focus

The project focuses on practical AI application engineering rather than model training. Key areas include:

* LLM application development
* Tool/function calling
* Agent orchestration
* Retrieval-augmented generation
* Structured outputs
* Context management
* Streaming responses
* Guardrails
* Basic LLM evaluation
* Integration with enterprise-style data systems

The billing, infrastructure, and policy data used in this project are synthetic and intended for demonstration purposes.

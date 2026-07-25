# UK Visa Guidance Agent

## Project Overview

The UK Visa Guidance Agent is an AI-powered assistant designed to help immigration consultants and visa caseworkers quickly retrieve accurate information from official GOV.UK visa guidance.

The agent combines Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), planning, tool selection, memory, and adaptive behaviour to provide grounded responses while reducing manual document searching.

---

## Features

- Gemini LLM integration
- Retrieval-Augmented Generation (RAG)
- Official GOV.UK visa guidance knowledge base
- ChromaDB vector database
- Semantic search using embeddings
- Multi-step planning
- Tool selection
- Short-term conversation memory
- Adaptive behaviour using user feedback
- Logging and graceful error handling

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| Language | Python 3.11 |
| LLM | Google Gemini |
| Framework | LangChain |
| Vector Database | ChromaDB |
| Embeddings | Gemini Embeddings |
| Development Environment | Google Colab |

---

## Repository Structure

```
UK-Visa-Guidance-Agent/
│
├── UK_Visa_Guidance.ipynb
├── requirements.txt
├── README.md
│
├── data/
│     Immigration Rules - Immigration Rules Appendix Skilled Worker - Guidance - GOV.UK.pdf
|     Immigration Rules - Immigration Rules_ Appendix Student - Guidance.pdf
|     Skilled Worker visa.pdf
|     Skilled_worker Guidance.pdf
|     Standard Visitor.pdf
|     Student visa.pdf
|     Visit Caseworker Guidance.pdf
|     guide to supporting documents.pdf
|     Immigration Rules - Guidance.pdf
|     Immigration Rules - Immigration Rules Appendix Finance - Guidance.pdf
│
├── docs/
│     Demo_Script.pdf
│     UK Visa Guidance & Document Readiness Agent.pdf
│     UK Visa Application Guidance & Document Readiness Evaluation.pdf
│     UK Visa Guidance Agent – Engineering & Product Justification.pdf
│     visa_agent_evaluation_metrics.xlsx
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/<your_username>/UK-Visa-Guidance-Agent.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Configure Gemini API

Create a Gemini API key from Google AI Studio.

Set the API key in Google Colab:

```python
from google.colab import userdata

API_KEY = userdata.get("GOOGLE_API_KEY")
```

Alternatively, use an environment variable when running locally.

---

## Running the Project

Open

```
visa_agent.ipynb
```

Run all cells from top to bottom.

The notebook will:

1. Load GOV.UK visa guidance
2. Split documents into chunks
3. Generate embeddings
4. Build the Chroma vector database
5. Initialise the tools
6. Start the AI agent

---

## Example Questions

- What documents are required for a Skilled Worker visa?
- Can my spouse accompany me?
- What financial evidence is required for a Student visa?
- I have a sponsor and passport. Am I eligible?
- What about my wife?

---

## System Architecture

```
User

↓

Planner

↓

Tool Selection

↓

Document Retrieval (RAG)

↓

Gemini LLM

↓

Memory

↓

Adaptive Behaviour

↓

Final Response
```

---

## Evaluation

The agent was evaluated using multiple scenarios including:

- RAG retrieval
- Tool selection
- Planning
- Memory
- Adaptive behaviour
- Out-of-domain questions
- Graceful failure handling

Detailed evaluation is available in:

```
docs/Evaluation_Report.pdf
```

---

## Limitations

- Uses only indexed GOV.UK guidance
- Requires a valid Gemini API key
- Does not provide legal advice
- Knowledge base must be refreshed when GOV.UK updates guidance

---

## Future Improvements

- Automatic document refresh
- OCR for uploaded documents
- Multi-language support
- Cloud deployment
- Authentication
- Analytics dashboard

---

## Author
Srinviasa Gudarada
Capstone Project
UK Visa Guidance Agent

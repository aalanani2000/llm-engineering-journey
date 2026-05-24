# 🧠 AI Job Description Analyzer

> **Day 1 Exercise — LLM Engineering Course** by [Ed Donner](https://github.com/ed-donner/llm_engineering)  
> Author: [Abdulrahman Alanani](https://linkedin.com/in/abdulrahman-alanani)

Paste any AI/ML job description and get an **instant, structured skill gap analysis** against your CV — powered by the OpenAI API and prompt engineering.

---

## What It Does

The analyzer reads a job description and returns:

- **Match score** (0–100%) with a verdict label
- **Skills you already have** matched against the JD
- **Gaps to close** — skills explicitly required that you lack
- **Transferable strengths** — your skills not in the JD but genuinely relevant
- **Prioritized action plan** — specific next steps to become a stronger candidate

**Sample output:**
```
============================================================
  ROLE    : Junior AI Engineer
  COMPANY : --------
  SCORE   : 63% — Partial Match
============================================================

📋 SUMMARY
  Abdulrahman has a strong practical foundation in Python, deep learning frameworks,
  and real-world model deployment on edge hardware. However, the role explicitly requires
  LLM application experience and RAG pipeline development, both of which are currently
  in progress. His Computer Vision and MLOps background transfers well, but he needs
  at least one shipped LLM project to be a competitive candidate.

✅ SKILLS YOU ALREADY HAVE
  • Python (Advanced) — core requirement, clearly demonstrated
  • PyTorch & TensorFlow — listed as required, strong CV evidence
  • Model deployment & monitoring — proven via drone project and work experience
  • Docker & CI/CD for AI — matches MLOps requirements
  • AWS & OCI cloud exposure — aligns with cloud infrastructure requirement
  • Git proficiency — confirmed

❌ GAPS TO CLOSE
  • LLM application development — no shipped LLM project yet
  • RAG pipeline experience — currently in progress (Week 1 of Ed Donner course)
  • Vector databases (Pinecone, ChromaDB, Weaviate) — not yet used
  • FastAPI or similar REST API framework — not listed in CV
  • LangChain or LlamaIndex — no experience yet

🔄 TRANSFERABLE STRENGTHS
  • Edge AI deployment — Raspberry Pi inference experience maps to resource-constrained LLM serving
  • Anomaly detection pipeline — shows ability to build and ship end-to-end ML systems
  • LLMOps certification — signals awareness of production LLM lifecycle

🎯 YOUR ACTION PLAN
  1. Complete and publish a RAG project (Week 3–4 of current course) — this single project
     closes the biggest gap on this JD
  2. Build a FastAPI wrapper around an LLM call and deploy it — shows backend integration skills
  3. Add ChromaDB to your RAG project as the vector store — covers the vector DB requirement
  4. Update your CV with the LLM course project as soon as it's complete

============================================================
```

## LLM Engineering Concepts Demonstrated

| Concept | Where |
|---|---|
| System prompt vs user prompt | Cells 4 & 6 |
| Static context injection | CV loaded into system prompt |
| Structured JSON output from LLMs | System prompt schema definition |
| Defensive output parsing | `removeprefix` + `json.loads` in Cell 8 |
| Token usage tracking | Cell 7 output |
| OpenAI-compatible local LLM support | Cell 7 comments (Ollama) |

---

## Project Structure

```
day1_exercise/
├── day1_jd_analyzer.ipynb   # Main notebook — run top to bottom
├── .env                     # Your API key (never commit this)
├── .gitignore               # Excludes .env from version control
└── README.md                # This file
```

---

## Setup

### Prerequisites

- Python 3.10+
- An OpenAI API key → [platform.openai.com](https://platform.openai.com)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/aalanani2000/llm-engineering-journey.git
cd llm-engineering-journey/day1_exercise

# 2. Install dependencies
pip install openai python-dotenv

# 3. Create your .env file
echo "OPENAI_API_KEY=sk-proj-your-key-here" > .env

# 4. Open the notebook
jupyter notebook day1_jd_analyzer.ipynb
```

### Run

Execute cells **top to bottom**. To analyze a different job description, edit the `sample_jd` string in **Cell 5** and re-run from Cell 5 onward.

---

## Running with a Free Local LLM (No API Key)

You can run this notebook entirely offline using [Ollama](https://ollama.com) — no API key or costs needed.

```bash
# 1. Install Ollama: https://ollama.com
# 2. Pull a model (choose one):
ollama pull llama3      # Meta Llama 3 8B   — best quality  (~5 GB)
ollama pull mistral     # Mistral 7B        — fast & capable (~4 GB)
ollama pull phi3        # Microsoft Phi-3   — lightest option (~2 GB)
```

Then in **Cell 7**, comment out Option A and uncomment Option B. No other changes needed — Ollama exposes an OpenAI-compatible API at `localhost:****`.

---

## Customizing for Your Own CV

The candidate CV is defined as a string constant in **Cell 3** (`CV_CONTEXT`).  
Replace the content with your own background to use this tool for your own job search.

> In a production version of this app, the CV would be loaded from a database or file — not hardcoded. The hardcoded approach is intentional here to keep Day 1 focused on prompt engineering fundamentals.

---

## Part of a Larger Journey

This is **Day 1** of my LLM engineering learning path. Each exercise builds toward production-grade AI applications.

| Day | Project | Concepts |
|---|---|---|
| Day 1 | **AI Job Description Analyzer** ← you are here | Prompt engineering, JSON output, OpenAI API |
| Coming soon | RAG Pipeline | Embeddings, vector databases, retrieval |
| Coming soon | LLM Agent | Tool use, memory, agentic workflows |

Follow along: [github.com/aalanani2000](https://github.com/aalanani2000)

---

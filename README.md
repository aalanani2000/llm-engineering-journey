# 🚀 LLM Engineering Journey

> **"Become an LLM Engineer in 8 Weeks"** — following the course by [Ed Donner](https://github.com/ed-donner/llm_engineering)  
> Built by [Abdulrahman Alanani](https://linkedin.com/in/abdulrahman-alanani) — AI Engineer based in Riyadh, Saudi Arabia

This repository documents my hands-on journey from Computer Vision engineer to production LLM engineer. Every folder contains a working project built during the course — not just notebooks with notes, but real tools with real output.

---

## 🗺️ Journey Map

| # | Project | Concepts | Status |
|---|---|---|---|
| Day 1 | [AI Job Description Analyzer](./day1_exercise/) | Prompt engineering · Structured JSON output · OpenAI API | ✅ Complete |
| Week 1 | [AI Technical Tutor](./Week%201%20exercise/) | Streaming API · Local LLMs · System prompt design | ✅ Complete |
| Week 2 | RAG Pipeline | Embeddings · Vector databases · Retrieval | 🔜 Coming soon |
| Week 3 | LLM Agent | Tool use · Memory · Agentic workflows | 🔜 Coming soon |
| Week 4 | Fine-tuning Pipeline | LoRA · QLoRA · HuggingFace · vLLM | 🔜 Coming soon |
| Week 5–8 | Production AI App | Full-stack · Deployment · Evaluation | 🔜 Coming soon |

---

## 🛠️ Projects

### Day 1 — AI Job Description Analyzer
Paste any AI/ML job description and get an instant skill gap analysis — match score, skills you have, gaps to close, and a prioritized action plan.

**Key engineering:** structured JSON output from LLMs, system/user prompt separation, defensive output parsing.  
→ [View project](./day1_exercise/)

---

### Week 1 — AI Technical Tutor
Ask any technical question and get a deep, structured explanation from two LLM backends simultaneously — OpenAI GPT with live streaming and a free local model via Ollama.

**Key engineering:** streaming API, `update_display` for live rendering, local LLM inference, expert system prompt design.  
→ [View project](./Week%201%20exercise/)

---

## 🧰 Tech Stack

As the journey progresses, this stack grows:

| Category | Tools |
|---|---|
| LLM APIs | OpenAI, Anthropic |
| Local LLMs | Ollama (Gemma4, Llama3, Mistral) |
| Frameworks | LangChain, LangGraph (coming) |
| Vector DBs | ChromaDB, Pinecone (coming) |
| Deployment | FastAPI, Docker (coming) |
| Cloud | AWS SageMaker, Oracle OCI |
| Languages | Python, C++ |

---

## 🏃 Getting Started

Each project folder is self-contained with its own README and setup instructions. The only shared requirement is an OpenAI API key.

```bash
# Clone the repo
git clone https://github.com/aalanani2000/llm-engineering-journey.git
cd llm-engineering-journey

# Each project has its own setup — see the folder README
cd day1_exercise
pip install openai python-dotenv
echo "OPENAI_API_KEY=sk-proj-your-key" > .env
```

---

## 👤 About Me

I'm an AI Engineer with a background in Computer Vision, edge AI deployment, and MLOps — currently expanding into LLM engineering, RAG systems, and agentic AI workflows.

- 🎓 B.Eng. Computer and Systems Engineering — Badr University Cairo
- 💼 AI/ML Systems Support Engineer — Problem Solver Org at Future of Egypt
- 📜 LLMOps Specialization — DeepLearning.AI
- 🌍 Based in Riyadh, Saudi Arabia — open to remote

**Connect:** [LinkedIn](https://linkedin.com/in/abdulrahman-alanani) · [GitHub](https://github.com/aalanani2000)

---

*Updated weekly as new projects are completed.*

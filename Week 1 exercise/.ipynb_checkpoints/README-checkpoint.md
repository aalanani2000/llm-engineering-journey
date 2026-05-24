# 🧠 Week 1 Exercise — AI Technical Tutor

> **Week 1 Exercise — LLM Engineering Course** by [Ed Donner](https://github.com/ed-donner/llm_engineering)  
> Author: [Abdulrahman Alanani](https://linkedin.com/in/abdulrahman-alanani)

A technical question-answering tool that explains any programming or AI concept in depth — powered by two LLM backends running side by side.

---

## What It Does

Ask any technical question and get a **structured, expert-level explanation** covering:

- High-level intuition
- Core concepts broken down
- Step-by-step reasoning
- Practical code examples
- Common mistakes and misconceptions
- Real-world engineering applications
- Concise summary

**Two backends, same question:**

| Backend | Model | Cost | Speed |
|---|---|---|---|
| OpenAI API | `gpt-5.4-mini` | Paid (fractions of a cent) | Fast + streams live |
| Ollama (local) | `gemma4` | Free | Depends on your hardware |

---

## LLM Engineering Concepts Demonstrated

| Concept | Where |
|---|---|
| System prompt engineering | Cell 5 — expert persona + response rules |
| User prompt templating | Cell 6 — structured output format via f-string |
| OpenAI streaming API | Cell 8 — `stream=True` + `update_display` |
| Local LLM inference | Cell 9 — Ollama with OpenAI-compatible format |
| Jupyter Markdown rendering | Cells 8 & 9 — `display(Markdown(...))` |
| Model constants pattern | Cell 3 — single place to swap models |

---

## Project Structure

```
week1_exercise/
├── week1_exercise.ipynb   # Main notebook — run top to bottom
├── .env                   # Your API key (never commit this)
├── .gitignore             # Excludes .env and cache files
└── README.md              # This file
```

---

## Setup

### Prerequisites

- Python 3.10+
- OpenAI API key → [platform.openai.com](https://platform.openai.com)
- Ollama (for the local model cell) → [ollama.com](https://ollama.com)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/aalanani2000/llm-engineering-journey.git
cd llm-engineering-journey/week1_exercise

# 2. Install Python dependencies
pip install openai python-dotenv ollama

# 3. Create your .env file
echo "OPENAI_API_KEY=sk-proj-your-key-here" > .env

# 4. Pull the local model (for Cell 9)
ollama pull gemma4

# 5. Open the notebook
jupyter notebook week1_exercise.ipynb
```

### Run

Execute cells **top to bottom**. To ask a new question, edit the `question` variable in **Cell 4** and re-run from Cell 4 onward — no need to re-run setup cells.

---

## Example Output

**Question asked:**
```python
question = """
Please explain what this code does and why:
yield from {book.get("author") for book in books if book.get("author")}
"""
```

**GPT response covers:**
- What `book.get("author")` does vs `book["author"]` — and why `.get()` is safer
- How the set comprehension `{...}` deduplicates authors automatically
- What `yield from` does and why it's preferred over a manual `for` loop
- The walrus operator `:=` as a cleaner alternative to calling `.get()` twice
- Memory implications: when to use a set vs a streaming generator for large datasets
- Real-world usage in ETL pipelines, API processing, and data engineering

---

## Key Engineering Insight

Comparing GPT and a local model on the **same prompt** is a practical evaluation technique. You'll notice differences in:
- Response depth and accuracy
- Formatting quality  
- Latency
- Cost (one is free)

This comparison skill — evaluating models against each other for a specific task — is something you'll use constantly when building production AI products.

---

## Part of a Larger Journey

| Exercise | Project | Concepts |
|---|---|---|
| Day 1 | [AI Job Description Analyzer](../day1_exercise/) | Prompt engineering, JSON output, OpenAI API |
| Week 1 | **AI Technical Tutor** ← you are here | Streaming, local LLMs, system prompt design |
| Coming soon | RAG Pipeline | Embeddings, vector databases, retrieval |
| Coming soon | LLM Agent | Tool use, memory, agentic workflows |

Follow along: [github.com/aalanani2000](https://github.com/aalanani2000)

---


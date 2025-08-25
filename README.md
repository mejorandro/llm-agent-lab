# 🌍 AgentFlow

AgentFlow is an **AI agent lab** built with LangChain + LangGraph.  
The first prototype is a **Daily AI Reader Agent**: it generates a 10-minute daily reading with fresh AI news, opportunities, daily actions, LinkedIn posts, POC ideas, and compounding strategy.

The vision: turn agent ideas into working prototypes, expose them as APIs, and consume them from Next.js/React projects to create **dynamic and scalable websites**.

---

## 🚀 Current Features
- Daily AI Reader Agent with:
  - Key AI news (summarized clearly)
  - Opportunities for Tech Lead & Full-Stack profiles
  - Daily actionable steps
  - Bilingual LinkedIn post drafts (Spanish + English)
  - 3 quick POC ideas
  - Compounding strategy explanation  

---

## 📂 Repository Structure
- `/agents` → contains your first agent (`daily_reader.py`).  
- `requirements.txt` → Python dependencies.  
- `README.md` → project overview.  
- `.gitignore` → standard ignores.  

*(In the future: `/prompts` for centralized multi-language prompts, `/api` for FastAPI endpoints, `/examples` for demos, etc.)*

---

## ⚡ Tech Stack
- **LangChain / LangGraph** → agent orchestration.  
- **OpenAI (gpt-4o)** → LLM backbone.  
- **Gradio** → quick UI prototyping.  

---

## 🛠️ Quickstart

```bash
# Create venv
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run demo
python agents/daily_reader.py

# 🌍 AgentFlow

AgentFlow is an **AI agent lab** built with LangChain + LangGraph.  
It’s a sandbox where ideas turn into **working MVPs**: small, functional agents that can later be exposed as APIs and consumed in Next.js/React projects to create **dynamic and scalable websites**.

The vision: build a **library of agents**, each one tackling a real-world use case, starting lean and evolving into production-ready tools.

---

## 🚀 Current MVP Agents (Catalog)

### 1. 📰 Daily AI Reader Agent (`agents/grow_pulse.py`)
Generates a 10-minute daily reading with:
- Key AI news (summarized clearly)
- Opportunities for Tech Lead & Full-Stack profiles
- Daily actionable steps
- Bilingual LinkedIn post drafts (Spanish + English)
- 3 quick POC ideas
- Compounding strategy explanation

👉 First prototype — the foundation of **GrowPulse**.

---

### 2. 🛠️ Weekend Support Agent (`agents/weekend_support.py`)
Connects to a Confluence space to act as an **internal weekend helper**:
- Retrieves docs from Confluence (via embeddings + FAISS)
- Summarizes docs in plain language
- Suggests one practical action (≤15 min)
- Provides a stitched **final support answer**
- ✅ Supports **Prompt Pages** (Confluence pages acting as agent instructions)  
  e.g. *AI-Agent: Service Desk Instructions*, *AI-Agent: Travel Experience Playbook*

👉 Example UI: [pura_vida_helper.ipynb](https://github.com/mejorandro/llm-agent-lab/blob/main/examples/pura_vida_helper.ipynb)

---

### 3. (Reserved slot for next MVP… 🚧)
Every new idea → becomes a small agent → added here.  
Some upcoming candidates:
- ✈️ Travel Experience Agent (for logistics team)
- 🧾 Finance Helper Agent (for invoices + billing FAQs)
- 👨‍💻 DevOps Incident Agent (on-call KB search)

---

## 📂 Repository Structure
- `/agents` → agent implementations (`daily_reader.py`, `weekend_support.py`, …).  
- `/examples` → demos and notebooks (`pura_vida_helper.ipynb`).  
- `requirements.txt` → Python dependencies.  
- `README.md` → project overview and agent catalog.  
- `.gitignore` → standard ignores.  

*(Planned: `/prompts` for centralized prompts, `/api` for FastAPI endpoints, `/tests` for agent tests.)*

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
```

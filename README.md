# 🌍 AgentFlow

AgentFlow is an **AI agent lab** built with LangChain + LangGraph.  
It’s a sandbox where ideas turn into **working MVPs**: small, functional agents that can later be exposed as APIs and consumed in Next.js/React projects to create **dynamic and scalable websites**.

The vision: build a **library of agents**, each one tackling a real-world use case, starting lean and evolving into production-ready tools.

---

## 🚀 Current MVP Agents (Catalog)

All current MVP agents live under the `/examples/` folder as Jupyter notebooks or Gradio demos.  

### 1. 📰 Grow Pulse Daily Reader (`examples/grow-pulse-daily-reader.ipynb`)
- Generates daily readings with 3–5 recent news items related to the user’s **profession** and **sector**.
- Extracts opportunities contextualized for the career path.
- Suggests one daily actionable step (≤15 min).
- Drafts bilingual LinkedIn posts (Spanish + English).
- Creates 3 visible mini-POCs (≤45 min).
- Explains how actions, posts, and POCs compound into career growth.

### 2. 🤖 AI Daily Reader / Career Coach (`examples/ai_daily_reader.ipynb`)
- Focuses specifically on **AI industry news** (OpenAI, Anthropic, DeepMind, OSS, enterprise adoption).
- Maps news items into opportunities for Tech Leads and Full-Stack profiles.
- Suggests one micro-action to get closer to global consulting opportunities (+10K/month).
- Drafts bilingual LinkedIn posts (authoritative, inspiring, non-egocentric).
- Provides POC ideas tied to AI and .NET scenarios.
- Explains how daily actions + posts + POCs compound strategically.

### 3. 🛠️ Weekend Support Agent (`examples/pura_vida_helper.ipynb`)
- Connects to Confluence space as a **weekend support helper**.
- Retrieves docs (via embeddings + FAISS).
- Summarizes docs in plain language.
- Suggests one practical action (≤15 min).
- Provides a stitched **final support answer**.
- ✅ Supports **Prompt Pages** (special Confluence pages that act as agent instructions).  
  e.g. *AI-Agent: Service Desk Instructions*, *AI-Agent: Travel Experience Playbook*

### 4. 🧠 Grow Routine – Nutrition & Lifestyle Validator (`examples/grow-routine-5-spanish-validador.ipynb`)
- Spanish-first multi-role agent combining:  
  - 🏋️ **Coach** → Generates physical & lifestyle recommendations.  
  - 🥦 **Nutritionist** → Creates nutrition plan with macros, calories, considerations (fasting, allergies), and technical justification.  
  - 🔎 **Macro Validator** → Validates consistency of macros, calories, and reasoning.  
- Conditional loop: nutrition plan regenerates automatically if validation fails.  
- Outputs a **final Markdown summary**: plan + validation + motivational note.  
- ✅ Interactive **Gradio UI** for InBody + goals input → final structured plan output.

---

## 📂 Repository Structure
- `/examples` → contains MVP agent notebooks (`grow-pulse-daily-reader.ipynb`, `ai_daily_reader.ipynb`, `pura_vida_helper.ipynb`).  
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

# Run any notebook demo
jupyter notebook examples/grow-pulse-daily-reader.ipynb
```

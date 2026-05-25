# AI Research & Writing Agent
### Built with CrewAI · LangChain · Google Gemini

A multi-agent AI system that autonomously researches any topic and produces a polished, LinkedIn-ready summary post — powered by **CrewAI**, **LangChain**, and **Google Gemini**.

---

## What It Does

You give it a topic. Three specialized AI agents take over:

1. **Researcher** — Gathers latest facts, trends, and insights on the topic
2. **Summarizer** — Condenses research into clean, readable bullet points
3. **Writer** — Crafts a professional summary post ready for LinkedIn or a blog

The final output is printed to the console **and saved as a `.txt` file**.

---

## Project Structure

```
crew_ai_agent_(lc&lg).py
│
├── 1. Basic Agent          → Single motivational speaker agent
├── 2. Custom Input         → Dynamic topic input via {topic} variable
├── 3. Multi-Agent          → Researcher + Summarizer (current affairs)
├── 4. Human in the Loop    → Personalized motivational messages
└── 5. Main Project ✅      → Full 3-agent Research Summary Generator
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| [CrewAI](https://github.com/joaomdmoura/crewAI) | Multi-agent orchestration |
| [LangChain](https://www.langchain.com/) | LLM tooling & integrations |
| [Google Gemini](https://ai.google.dev/) | LLM backbone (`gemini-2.0-flash`) |
| Python 3.10+ | Runtime |
| Google Colab | Development environment |

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

### 2. Install dependencies

```bash
pip install -qU "langchain[google-genai]" langchain-google-genai crewai "crewai[tools]"
```

### 3. Set your API key

If running locally, set your Google API key as an environment variable:

```bash
export GOOGLE_API_KEY="your_api_key_here"
```

If running on **Google Colab**, add it under `Secrets` (the 🔑 key icon) with the name `GOOGLE_API_KEY`.

### 4. Run it

```bash
python crew_ai_agent_\(lc\&lg\).py
```

You'll be prompted to enter a topic:

```
Enter a topic you want the AI to research and summarize: Artificial Intelligence in Healthcare
```

The agents will then run sequentially and output a polished summary post.

---

## Sample Output

```
FINAL RESEARCH SUMMARY POST:

• AI is transforming diagnostics with 94% accuracy in detecting certain cancers...
• Predictive analytics is reducing hospital readmissions by up to 30%...
• ...

[LinkedIn post written by the Writer agent]

Saved your summary post as 'research_summary_Artificial_Intelligence_in_Healthcare.txt'
```

---

## API Key Required

This project uses **Google Gemini** via the Gemini API.

Get your free API key here → [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)

---

## Output

The final summary is saved automatically as:

```
research_summary_<your_topic>.txt
```

---

## Known Limitations

- No live web search (FirecrawlSearchTool integrated but not active — agents rely on Gemini's built-in knowledge)
- Best results for topics within Gemini's training data
- Rate limits may apply on the free Gemini API tier

---

## 🙋 Author

**Pavan** — AI & ML Engineer  
B.Tech in AI & ML · Siddharth Institute of Engineering and Technology  
[LinkedIn](https://linkedin.com/in/YOUR_PROFILE) · [GitHub](https://github.com/YOUR_USERNAME)

---

##  License

MIT License — free to use, modify, and distribute.

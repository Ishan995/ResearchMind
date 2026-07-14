# ResearchMind

A polished multi-agent research assistant built with Python, LangChain, Groq, Tavily, and Streamlit. The system searches the web, scrapes relevant sources, drafts a research report, critiques it, and then lets the user ask follow-up questions in the same session.

## Why this project stands out

ResearchMind demonstrates a practical end-to-end AI workflow that combines:

- multi-agent orchestration for specialized tasks
- real web search and scraping
- LLM-powered report generation and review
- an interactive Streamlit interface for a polished user experience
- Groq-based model integration for fast and cost-effective inference

This project is a strong example of agentic AI engineering, prompt design, tool use, state management, and product-style UI building in a single, cohesive application.

## Project Highlights

- Search Agent: gathers recent and reliable information from the web
- Reader Agent: scrapes and extracts content from selected URLs
- Writer Chain: drafts a structured research report
- Critic Chain: reviews the report and provides feedback
- Chat Assistant: answers follow-up questions using the collected research context

## Tech Stack

- Python
- LangChain
- LangChain Groq integration
- Groq API
- Tavily API
- BeautifulSoup
- Requests
- Streamlit
- Python-dotenv

## Project Structure

```text
.
├── agents.py          # LLM agent and chain definitions
├── app.py             # Streamlit web application
├── pipeline.py        # CLI-style research pipeline runner
├── tools.py           # Web search and scraping tools
├── requirements.txt   # Python dependencies
├── .env               # Environment variables (not committed)
└── README.md          # Project documentation
```

## Setup Instructions

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/ResearchMind.git
   cd ResearchMind
   ```

2. Create and activate a virtual environment
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file with your API keys
   ```env
   GROQ_API_KEY=your_groq_api_key
   TAVILY_API_KEY=your_tavily_api_key
   ```

5. Run the app
   ```bash
   streamlit run app.py
   ```

## How it works

1. The user enters a research topic.
2. The Search Agent finds recent and relevant information.
3. The Reader Agent scrapes a key source for deeper context.
4. The Writer Chain builds a structured research report.
5. The Critic Chain evaluates the report and offers feedback.
6. The user can ask follow-up questions and receive answers based on the current research context.

### System Flow

```text
User Input
   ↓
Search Agent → Web Results
   ↓
Reader Agent → Scraped Content
   ↓
Writer Chain → Research Report
   ↓
Critic Chain → Review & Feedback
   ↓
Chat Assistant → Follow-up Q&A
```

### Architecture Overview

```text
Streamlit UI
   ↓
Agents / Chains (LangChain)
   ↓
Tools (Tavily + Web Scraping)
   ↓
Groq LLM
```

## Example Use Cases

- Market research summaries
- Academic topic exploration
- News and trend analysis
- Product research and competitor analysis
- AI-powered knowledge assistant workflows

## Future Improvements

- Add vector database-based retrieval for more scalable knowledge search
- Add source citations in chatbot answers
- Improve memory and conversation continuity
- Support multi-document research workflows
- Add authentication and user history

## License

This project is licensed under the MIT License.

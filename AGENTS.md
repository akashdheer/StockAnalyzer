# AGENTS.md - Constitution for Codex Agent
Project Name: Investment Grade Stock Analyser
Version: 1.0
Last Updated: 2026-03-09

## 1. Project Overview
We are building a clean, professional web app that lets any user type a stock ticker (e.g. RELIANCE.NS or AAPL) and instantly see:
- Live price and all important ratios
- Investment Grade Score (0-100) with clear explanation
- Interactive chart
- News + sentiment
- Peer comparison
- PDF export
- Watchlist

Big red disclaimer on every page: “This is not financial advice. For educational purposes only.”

Goal: The final app must be simple enough that a complete beginner who can only read Python can understand every single file.

## 2. Tech Stack (NEVER change without my explicit approval)
- Language: ONLY Python 3.12 (no JavaScript, no TypeScript, no HTML, no React)
- Web Framework: Streamlit (latest version) — everything must be in Python
- Data Library: pandas + yfinance (free, no API key needed for most things)
- Charts: Plotly (beautiful interactive charts, pure Python)
- PDF Export: reportlab or streamlit-pdf (pure Python)
- Database (for watchlist): SQLite (simple file-based, no extra setup) or Supabase only if I say so later
- Deployment: Streamlit Community Cloud (free)
- Agents and Tools : Langgraph Libraries 
- Additional libraries (only when needed): numpy, plotly, yfinance, pandas, reportlab, python-dotenv
- NEVER use: FastAPI, Flask, Next.js, Tailwind, any frontend framework

All code must stay in simple Python files only.

## 3. Coding Standards - Keep It Super Simple & Beginner Friendly
- Use only basic Python (no advanced tricks, no list comprehensions if a for-loop is clearer)
- Every function must have a clear docstring explaining:
  - What it does
  - What inputs it takes
  - What it returns
  - Example usage
- Add a comment above EVERY 3-5 lines explaining what that block does (in plain English)
- Variable names must be super clear: e.g. `investment_grade_score`, `current_price`, `five_year_eps_growth`
- Never use abbreviations without explaining them first
- Error handling: Always show friendly messages to the user (e.g. “Sorry, this stock is not available right now”)
- Keep every Python file under 200 lines if possible (split into small files)
- Use type hints only when they make code clearer (optional for beginners)

Example of good style (you must follow this):
```python
def calculate_investment_grade_score(data: dict) -> int:
    """Calculates Investment Grade Score out of 100.
    Rules are fixed - never change them.
    Returns a number between 0 and 100."""
    score = 0
    # Rule 1: Good ROE
    if data.get("roe", 0) > 15:
        score += 20
    # ... more rules
    return score
```

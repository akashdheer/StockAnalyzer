File Structure:
stock-analyser/
├── Brain                   # This folder contains both agents and tools folder
      ├── Agents            # This folder contains all the files that are agents or autonomous systems
      ├── Tools             # This folder contains all files that acts as tools for agents
├── app.py                  # Main Streamlit app (the website)
├── stock_data.py           # All functions to fetch data from yfinance
├── scoring.py              # All Investment Grade Score calculations
├── pdf_export.py           # Creates PDF report
├── utils.py                # Helper functions
├── PROJECT_MAP.md          # This file (auto updated by you)
├── AGENTS.md               # Rules you are reading now
└── requirements.txt

Data Flow:
User types ticker → app.py calls stock_data.py → scoring.py calculates score → plotly chart → displayed + PDF button

Features Done:
- Live price & basic ratios
- Investment Grade Score

Features To Do:
- Watchlist
- News section
5. Investment Grade Score Rules (FIXED - Never invent new ones)
Use exactly

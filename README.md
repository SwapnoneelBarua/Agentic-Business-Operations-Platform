# OpsPilot AI — Agentic Business Operations Platform

OpsPilot AI is a modular platform scaffold for agent-assisted business operations. It is designed to grow from a local MVP into a production-style application.

## Stack

- FastAPI and Pydantic for the API
- LangGraph for agent workflows
- PostgreSQL and SQLAlchemy for persistence
- Streamlit for the operator interface

## Quick start (Windows PowerShell)

1. Create a virtual environment and install the project:

   ```powershell
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   python -m pip install --upgrade pip
   pip install -e ".[dev]"
   ```

2. Copy `.env.example` to `.env` and adjust values as needed.
3. Start the API:

   ```powershell
   uvicorn app.main:app --reload
   ```

4. Open `http://127.0.0.1:8000/docs`. The health check is at `/api/v1/health`.
5. In another terminal, launch the Streamlit interface with `streamlit run frontend/app.py`.

To start the API and PostgreSQL with Docker Compose, run `docker compose up --build`.

## Project layout

- `app/`: API, persistence, agent, tool, service, integration, and observability modules
- `frontend/`: Streamlit operator interface
- `tests/`: unit, integration, security, and evaluation test suites
- `evals/`: agent evaluation runner and sample dataset
- `data/sample/`: sample CSV input data
- `scripts/`: database setup utilities
- `migrations/`: database migration environment
- `docs/`: architecture, API, security, and evaluation notes

Most business-operation modules are intentionally scaffolds; implement domain behavior as the project requirements become concrete.

## Development

Run tests with `pytest`. API configuration is read from environment variables; see `.env.example`.

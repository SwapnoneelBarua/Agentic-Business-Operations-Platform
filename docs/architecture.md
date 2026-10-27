# Architecture

OpsPilot AI is organized as a modular Python application. FastAPI exposes versioned HTTP endpoints; services coordinate business operations; repositories and SQLAlchemy models own persistence; LangGraph nodes and tools implement agent workflows; Streamlit provides the operator interface.

Consequential actions should pass through approval services and leave an audit trail. The initial scaffold only implements a health endpoint; domain workflows and persistence are intentionally not yet wired.

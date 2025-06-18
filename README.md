# Multi-Tool Agent (ADK Quickstart)

This repository contains a simple multi-tool agent built using Google’s Agent Development Kit (ADK). The agent can answer queries about the **weather** and the **current time** in a city, with a working web-based dev UI and terminal interface.

---

## 🚀 Prerequisites

- **Python** ≥ 3.9, or **Java** ≥ 17
- Virtual environment tool (e.g. `venv`) for Python
- CLI tools for Java (`maven` or `gradle`)
- A Google API key (Gemini LLM or Vertex AI)
  - Enable Vertex AI
  - Set environment variables or `.env` file

---

## 🔧 Installation

### Python setup

```bash
# 1. Create & activate virtual environment
python -m venv .venv
source .venv/bin/activate           # macOS/Linux
# .venv\Scripts\Activate.ps1        # Windows PowerShell

# 2. Install ADK
pip install google-adk

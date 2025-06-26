# Agent Development Kit (ADK) Quickstart 🧠

This repository provides a minimal example to create a multifunctional agent using Google’s Agent Development Kit (ADK), enabling time and weather queries.
https://google.github.io/adk-docs/ (google adk documentation)

## 📦 Prerequisites

- **Python** 3.9+ *or* **Java** 17+  
- Terminal access and a local IDE (e.g., VS Code, PyCharm, IntelliJ)  
- API access to a Gemini‑based LLM (via Google AI Studio or Vertex AI)

---

## 1. Install & Activate

### Python


python -m venv .venv
# Activate the virtual environment
source .venv/bin/activate           # macOS/Linux
.venv\Scripts\activate.bat          # Windows CMD
.venv\Scripts\Activate.ps1          # Windows PowerShell

pip install google-adk

Java**
Use Maven or Gradle to add ADK dependencies in your pom.xml or build.gradle.
Refer to the [ADK docs] quickstart for exact dependency coordinates

Create Agent Project
multi_tool_agent/
├── __init__.py
├── agent.py
└── .env

__init__.py:
from . import agent
agent.py: Defines tool functions (get_weather, get_current_time) and instantiates an Agent with these tools
.env: Stores authentication keys 

LLM Configuration & Authentication
Ensure you have credentials set up:
{For Gemini via API Key
GOOGLE_GENAI_USE_VERTEXAI=FALSE
GOOGLE_API_KEY=YOUR_API_KEY_HERE}
{For Vertex AI
GOOGLE_GENAI_USE_VERTEXAI=TRUE
GOOGLE_CLOUD_PROJECT=YOUR_PROJECT_ID
GOOGLE_CLOUD_LOCATION=YOUR_LOCATION}
For Java, replace these with corresponding environment variables

Running the Agent
Launching Dev UI (Python):
cd parent_folder
adk web

Open http://localhost:8000

Select your agent (e.g., multi_tool_agent)

Chat interactively or enable voice/video streaming after switching to a Gemini Live model

Example Prompts
“What is the weather in New York?”

“What is the time in New York?”

“What is the weather in Paris?”

“What is the time in Paris?”

#*Project Structure*
parent_folder/
├── multi_tool_agent/
│   ├── __init__.py
│   ├── agent.py
│   └── .env
├── .venv/                 # (optional, if you used virtual environment)
├── requirements.txt       # (optional, if you created one for dependencies)
├── README.md
└── any other scripts or config files



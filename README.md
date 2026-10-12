# Deep Research Agent

An AI-powered research application built with Python, the OpenAI Agents SDK, and Gradio.

Deep Research takes a user query, creates a research plan, gathers information from the web, and generates a structured research report. It can also deliver the final report through a configured messaging channel.

## Features

* **Research planning:** Breaks a research question into targeted web searches.
* **Parallel research:** Runs multiple searches concurrently.
* **Report generation:** Produces a structured report with a summary and follow-up questions.
* **Interactive interface:** Provides a Gradio web interface to submit research requests and follow progress.
* **Report delivery:** Supports email or Pushover notifications, depending on the configuration.

## Tech Stack

* Python
* OpenAI Agents SDK
* OpenAI API
* Gradio
* Pydantic
* Python `asyncio`

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/deep-research-agent.git
cd deep-research-agent
```

Replace `YOUR_USERNAME` with your GitHub username after creating the repository.

### 2. Create and activate a virtual environment

**Windows (PowerShell):**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root. Add your own credentials using the variable names expected by the application:

* `OPENAI_API_KEY`
* `DEFAULT_MODEL_NAME`
* `HOW_MANY_SEARCHES`
* `USE_EMAIL`
* `PUSHOVER_USER`
* `PUSHOVER_TOKEN`
* `EMAIL_SMTP_SERVER`
* `EMAIL_APP_PASSWORD`
* `EMAIL_ADDRESS`

Only configure the credentials required by your chosen delivery method. Never commit `.env` or expose API keys and passwords publicly.

### 5. Run the application

```bash
python app.py
```

Open the local Gradio URL displayed in your terminal.

## Project Structure

```text
deep-research-agent/
├── app.py
├── simple.py
├── planner_agent.py
├── search_agent.py
├── writer_agent.py
├── email_agent.py
├── messenger.py
├── research_manager.py
├── styles.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Roadmap

* Improve research autonomy through iterative searches.
* Strengthen source tracking and citation quality.
* Add robust error handling and execution limits.
* Evaluate report quality, execution time, and API costs.
* Expand the agent's tools and research capabilities progressively.

## Security

Store credentials in environment variables. Do not publish `.env`, API keys, passwords, or private user data.

## Status

A working prototype under active development. Features and architecture may evolve as the research agent becomes more autonomous.

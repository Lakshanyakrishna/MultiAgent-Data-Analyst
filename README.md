# Multi-Agent Data Analyst

Automated Profiler → EDA → AutoML → Verifier → Notebook Synthesizer → Gemini Insights

Track: Enterprise Agents

Tech: Python, Streamlit, Gemini, MCP Tools, A2A Bus, Multi-Agent Architecture

# Overview

The Multi-Agent Data Analyst is a fully automated, end-to-end data analysis pipeline powered by multiple specialized agents working together.
It uploads a dataset, analyzes it, builds ML models, verifies the results, generates notebooks, and produces final insights — without any manual coding.

This project demonstrates:

✔ Multi-agent systems

✔ A2A (Agent-to-Agent) 

✔ Tool-based agent execution (MCP Tools)

✔ Sessions & memory

✔ Context-aware notebook synthesis

✔ Gemini-powered explanations

✔ Streamlit multi-page application


# Problem Statement

Performing data analysis typically requires switching between tools, writing repetitive code, running models manually, validating outputs, and documenting everything.

For beginners, this is overwhelming.

For analysts, it's time-consuming.

For teams, it’s inconsistent.

# Goal: Build an agentic system that automates the entire workflow — from raw data to verified insights and notebook generation.

# Why Agents?

Agents make the system:

 -> Modular — each agent does one job

 -> Autonomous — actions happen without the user triggering each step

 -> Traceable — every step is observable

 -> Composable — agents communicate using A2A bus

 -> Extensible — new agents (e.g., Gemini Reviewer) can be added anytime

Instead of one giant notebook, the intelligence is distributed:

# Agent Roles

 -> Profiler Agent – inspects dataset, finds issues

 -> EDA Agent – generates charts, summaries, anomalies

 -> Model Agent (AutoML) – builds ML pipelines automatically

 -> Verifier Agent – detects inconsistencies, bad models, missing columns

 -> Notebook Synthesizer Agent – creates a clean notebook combining all outputs

 -> Gemini Agent – explains the ML results in human-friendly language

# Each agent writes outputs to memory → A2A orchestrates → Next agent reacts.

# Architecture

<img width="2452" height="1286" alt="image" src="https://github.com/user-attachments/assets/92641b2f-fceb-493a-b481-345e5e341de4" />


#  Components

✔  A2A Bus: lightweight JSON-based messaging bus

✔  MCP Tools: FileTools, DatasetTools, MemoryTools

✔  Streamlit UI: Multi-page dashboard

✔  Persistent storage: streamlit_app_storage/

✔  Notebook generation: nbformat + Markdown blocks

✔  Modeling: scikit-learn pipelines + RandomizedSearchCV

✔  LLM: Gemini 1.5 Flash / Pro for explanations

# Features

✔ Data Upload & Storage

✔ CSV upload

✔ Saved using FileTools + MemoryTools

✔ Profiler Agent

✔ Dataset size

✔ Missing values

✔ Memory footprint

✔ Column types

✔ EDA Agent

✔ Distribution plots

✔ Correlation heatmaps

✔ Outlier detection

✔ Saves charts to storage

✔ AutoML Model Agent

✔ Task detection (classification vs regression)

✔ Train/test split

✔ Numeric + categorical pipelines

✔ Hyperparameter search

✔ Saves model + metrics

✔ Verifier Agent

✔ Sanity checks

✔ Missing column checks

✔ Confidence output

✔ Notebook Synthesizer Agent

-> Generates a full .ipynb notebook

-> Includes profiler, EDA, model, and verifier outputs

-> Clean formatting

✔ Gemini Insights

-> Explains ML results in simple language

-> Suggests improvements

-> Highlights model strengths/weaknesses

# Tech Stack
Component	Technology
UI	Streamlit Multi-Page App
Agents	Python-based custom agents
A2A	JSON-based message bus
Tools	MCP Tools (FileTools, DatasetTools, MemoryTools)
Modeling	scikit-learn, pandas, numpy
Visualization	matplotlib, seaborn
Notebook	nbformat
LLM	Gemini 1.5 Flash
🚀 Deployment
✔ Streamlit Cloud (Recommended)

Push this repo to GitHub

Add GEMINI_API_KEY in Streamlit → Settings → Secrets

Select streamlit_app/app.py as entry point

Deploy 🎉

Environment Variables
GEMINI_API_KEY = "your-key"

🗂 Project Structure
multiagent-data-analyst/
│
├── src/
│   ├── agents/
│   ├── core/
│   ├── tools/
│   │   ├── file_tools.py
│   │   ├── dataset_tools.py
│   │   ├── memory_tools.py
│   │   ├── model_tools.py
│   │   └── notebook_tools.py
│
├── streamlit_app/
│   ├── app.py
│   └── pages/
│       ├── AutoML.py
│       ├── Profiler.py
│       ├── EDA_Dashboard.py
│       ├── Notebook_Report.py
│       ├── Verifier.py
│       └── A2A_Dashboard.py
│
├── streamlit_app_storage/
│   ├── memory/
│   ├── uploads/
│   └── reports/
│
└── README.md

💡 Future Improvements

Add RAG-based “Data Question Answering Agent”

Add deployment on Google Cloud Run using Docker

Add Evaluation Agent for model fairness

Provide more AutoML models (XGBoost, LightGBM)

Add voice-based interaction mode

🏅 Credits

Built by Vaishnavi Sharma as part of
Google x Kaggle – Agents Intensive (Nov 2025)

If you find this useful, ⭐ star the repo!

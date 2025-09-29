Academic Research Agent with Gemini & ExaTools

This project implements an AI-powered academic research agent that leverages Google Gemini for language understanding and ExaTools for scholarly data retrieval. The agent can automatically generate structured research reports on recent developments in any academic field.

Features

Integrates Gemini (gemini-1.5-pro) for advanced language generation.

Uses ExaTools to access academic publications and keywords.

Automatically generates research reports with:

Abstract

Introduction

Methodology

Literature Review

Analysis

Future Directions

Conclusions

References

Supports streaming responses for live research insights.

Saves generated reports in Markdown format.

Requirements

Python 3.10+

agno
 library

ExaTools

Google Gemini API Key

EXA API Key

Install dependencies:

pip install agno exa-py

Setup

Clone the repository (or open in Colab).

Set API keys:

import os
from getpass import getpass

# Securely input your Gemini API key
os.environ["GOOGLE_API_KEY"] = getpass("Enter your Gemini API key: ")

# Securely input your EXA API key
os.environ["EXA_API_KEY"] = getpass("Enter your EXA API key: ")


Run the agent script:

!python research_agent.py

Usage

The agent can generate research reports on any topic. Example:

research_scholar.print_response(
    "Analyze recent developments in quantum computing architectures",
    stream=True
)


Reports are automatically saved in the tmp/ directory as Markdown files.

Stream mode allows you to see the report being generated in real time.

File Structure
.
├── research_agent.py       # Main script for the AI research agent
├── tmp/                    # Folder where generated Markdown reports are saved
└── README.md               # Project documentation

Notes

Remove emojis or non-ASCII characters in descriptions and instructions to avoid encoding errors.

Ensure API keys are kept secret and never pushed to public repositories.

Colab users must re-enter API keys after restarting the runtime.

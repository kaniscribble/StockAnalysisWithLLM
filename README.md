# Document Summarization and Analysis with LangChain, LangGraph, and ReAct Agent

This project implements a pipeline using LangChain, LangGraph, and a ReAct-based agent to process transcript documents. It loads and chunks input files, summarizes them incrementally using an LLM (via Ollama), removes redundancy, and leverages tools such as web search and Python code execution to provide detailed analysis and insights.

## Overview

The pipeline performs the following steps:

1. Load the transcript.
2. Split the documents into manageable chunks.
3. Summarize each chunk incrementally using a local LLM.
4. Append each new summary to the existing summary, then re-summarize to remove redundancy.
5. Pass the final summary to a ReAct agent.
6. The agent uses reasoning and tool use (web search or Python code execution) to further analyze the content.
7. Output the final summary and insights.

## Components

- **LangChain**: For prompt chaining, memory, and agent orchestration.
- **LangGraph**: For managing flow control and stateful iteration across document chunks.
- **Ollama**: To run local LLMs such as Mistral or LLaMA for summarization tasks.
- **ReAct Agent**: A reasoning agent that selects tools and performs contextual analysis.
- **Web Search Tool**: Allows the agent to fetch additional context from the web.
- **Python Tool**: Used by the agent for calculations, plots, or other code-based tasks.

## Installation

1. Clone the repository:

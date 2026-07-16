# AI Underwriting Assistant Agent
Building an AI Agent with RAG and LangChain

---

## Overview
This is a comprehensive single-file prototype demonstrating:

- RAG (Retrieval Augmented Generation) with document search
- Multi-tool Agent with underwriting guidelines search and, calculator
- Local execution with OpenAI's gpt model
- Conversational memory for context retention
  
---

## Features
Agent Tools
1. Document QA - RAG-based question answering on LangChain documentation
2. Alcohol Calculator - Safe mathematical calculations with alcohol formula

RAG System
- Loads and indexes LangChain documentation
- Uses OpenAI's embedding model for semantic search
- Retrieves relevant context for questions

---

## Setup
1. Install dependencies:

pip install -r requirements.txt

2. Get Google API Key:

- Visit OpenAI website
- Create a new API key
- Copy .env.example to .env and add your key

3. Run the prototype:

cd agentic-ai-inmemorychat
python main.py

---

## Example Queries

### Document Search (RAG)
"What is RAG in LangChain?"
"Explain how to assess for Heart Murmur"
"Assess rating by the following case: female 25 years old with DM2, HbA1c 8%, drink alcohol 30 grams/day, no smoking. What is the total rating for this case?"

### Alcohol Calculations
"Calculate alcohol quantity for 2 glasses of Whiskey"
"Drinking 1 bottle of wine"
"How many gram if this person drink 3 can of beer"

---

## Architecture

User Query → Guardrails → Agent → Tool Selection → Tool Execution → Response
                ↓
            Memory Update
                ↓
         Context Retention

### Agent Flow
1. Question Analysis - Agent analyzes the user query
2. Tool Selection - Chooses appropriate tool(s)
3. Tool Execution - Executes selected tool with parameters
4. Result Processing - Processes and formats results
5. Response Generation - Provides final answer to user
   

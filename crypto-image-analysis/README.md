**n8n-Telegram-Crypto-Analyzer**

**Description**:
n8n workflow that receives a coin name via Telegram, fetches its chart image from the web, performs AI-powered technical analysis, and returns a summary along with the chart. Fully modular, secure, and importable for seamless crypto monitoring and decision support.
**
Overview**

This project is a fully automated crypto analysis workflow built on n8n, combining Telegram, web data fetching, and AI-powered chart analysis.

**Workflow Flow**:

User sends a message/coin name via Telegram

Workflow fetches the coin’s chart image from the web

AI analyzes chart trends, support/resistance, and indicators

Workflow formats and summarizes results

Sends the chart + analysis back to Telegram

This single workflow handles end-to-end automation, making it ideal for traders, analysts, and crypto enthusiasts.

**Workflow Diagrams**

You can go through the images from the repository

**AI Chat Workflow**

Technical Analysis Workflow

Complete Workflow

The workflow files can be found in the workflows/ folder.

**Features**

Receive cryptocurrency names via Telegram

Fetch live chart images automatically

AI-powered chart analysis (trend detection, support/resistance, indicators)

Generate concise, readable summaries

Sends chart + analysis back to Telegram

Modular, secure, and easily importable

Configurable AI and web data sources

**Requirements**

n8n (self-hosted or cloud)

Telegram Bot credentials (Bot Token)

AI model credentials (OpenAI, Ollama, or another vision model)

Optional: API key for the web chart source

⚠️ No credentials included. Users must configure their own securely.

**Quick Start**

Clone the repository:

https://github.com/RukeshPallinti/n8n-telegram-image-analysis


Open n8n → Click Import Workflow

Upload the workflow file: Technical_Analyst_Workflow.json

Configure Telegram Bot and AI model credentials

Activate the workflow

Send a coin symbol/message via Telegram → Receive chart + AI summary

**API / Configuration**

The workflow uses external APIs and credentials. You must replace placeholders in the workflow JSON:

OpenRouter API Key

Telegram API Key

OpenAI API Key

Chart Image API Key

Make sure no secret keys are committed to GitHub. All credentials should be configured via n8n Credentials tab.

**Use Cases**

Rapid technical chart analysis for crypto traders

AI-assisted summaries for research or educational purposes

Automated monitoring of cryptocurrency charts

Quick insights without manual chart inspection

⚠️ Informational purposes only – not financial advice.

**Folder Structure**
n8n-telegram-crypto-analyzer/
│── workflows/
│   └── image_telegram_analysis.json   # Main workflow
│ai_chat_workflow.png
│technical_analysis_workflow.png
│complete_workflow.png
│── README.md                          # Project documentation
│── LICENSE                            # MIT License

**How It Works (Step-by-Step)**
1️⃣ Telegram Chat & AI Workflow

Goal: Talk to users and respond like a friendly financial assistant.

Steps:

User sends a message on Telegram

Telegram Trigger receives the message

AI Agent (via OpenRouter) reads the message and generates a conversational response

If the message mentions a stock ticker, the AI can call the Technical Analysis workflow to generate charts

Send Analysis sends the AI response back to Telegram

APIs Used:

OpenRouter → generates AI chat responses

Telegram → send/receive messages

2️⃣ Technical Analysis & Chart Workflow

Goal: Create stock charts, analyze them, and send insights

Steps:

Workflow Input Trigger receives the stock ticker from the AI Agent

Set Ticker formats the ticker for the chart API

Get Chart URL calls the Chart Image API to generate the chart

Download Chart downloads the chart image

Technical Analysis (OpenAI) analyzes the chart for trends, patterns, and key insights

Send Chart sends the chart image to Telegram

response sends the written analysis to Telegram

APIs Used:

OpenAI → technical chart analysis

Chart Image API → generate chart

Telegram → send chart & text

3️⃣ How the Workflows Connect

The AI Chat workflow is the main interface with users

When stock analysis is needed, the AI triggers the Technical Analysis workflow

Users get both:

Text analysis from AI (via OpenRouter)

Chart images showing stock trends

“And that’s it — after this, you’re all set and good to go!” ✅

**License**

MIT License – Free to use, modify, and distribute

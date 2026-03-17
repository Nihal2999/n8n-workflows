# 🔄 AI Automation Workflows — n8n

3 production-ready AI automation workflows built with n8n.

## Workflows

### 1. 📧 AI Email Classifier
Receives email text via webhook → classifies category and urgency → drafts reply.
- Categories: URGENT, BILLING, SUPPORT, SALES, HR, SPAM, INFO
- Returns: category, urgency, summary, suggested reply
- Trigger: POST webhook

### 2. 📰 Daily AI News Digest  
Runs every day at 9am → fetches top AI news → summarises with Groq → returns digest.
- Source: NewsAPI
- Returns: 5-story digest with sources
- Trigger: Schedule (daily 9am)

### 3. 📊 CSV Data Analyser
Receives CSV data via webhook → analyses patterns → returns actionable insights.
- Returns: trends, outliers, top 3 insights, data quality observations
- Trigger: POST webhook

## Setup

1. Import any `.json` file into n8n
2. Add your credentials:
   - Groq API Key (Header Auth)
   - NewsAPI Key (Query Auth)
3. Activate the workflow

## Stack
n8n · Groq API (Llama 3.3 70B) · NewsAPI · JavaScript
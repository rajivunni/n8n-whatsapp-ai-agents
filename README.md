# n8n WhatsApp AI Agents

A collection of n8n workflows that deploy AI-powered WhatsApp agents for service businesses. Each workflow connects WhatsApp Business API to an LLM-backed agent with persistent memory and a RAG knowledge base.

## Workflows

### WhatsApp HVAC Missed Call Handler
Triggers when a customer messages after a missed call. An OpenAI-powered agent responds with contextual answers pulled from a Supabase vector store (product/service knowledge base) and maintains conversation history via Postgres chat memory. Replies are sent back through the WhatsApp Business API.

**Stack:** WhatsApp Trigger, OpenAI GPT-4, Supabase Vector Store, Postgres Chat Memory, Google Sheets

### WhatsApp HVAC Product Expert
A persistent product expert bot for HVAC companies. Handles inbound WhatsApp enquiries about products, services, and pricing. Uses RAG to pull from a structured knowledge base so answers stay accurate and on-brand.

**Stack:** WhatsApp Trigger, OpenAI GPT-4, Supabase Vector Store, Embeddings, Postgres Memory

### WhatsApp SaaS Product Expert (B2B Demo)
A B2B-focused demo workflow for SaaS companies. Handles inbound WhatsApp leads, answers product questions, and qualifies prospects. Built to be adapted for client demos.

**Stack:** WhatsApp Trigger, OpenAI GPT-4, Supabase Vector Store, Embeddings, Postgres Memory

## Tech Stack

- [n8n](https://n8n.io) - workflow automation
- OpenAI GPT-4 - LLM
- Supabase - vector store for RAG
- PostgreSQL - conversation memory
- WhatsApp Business API
- Google Sheets - config/logging

## Usage

1. Import the `.json` file into your n8n instance via **Workflows > Import from file**
2. Configure credentials: OpenAI API key, WhatsApp Business API, Supabase project URL + key, Postgres connection
3. Populate your Supabase vector store with your knowledge base content
4. Activate the workflow

## About

Built by [Rajiv Unnikrishnan](https://www.rajivunnikrishnan.com) - n8n automation specialist.

# outlook-email-automation

An automated email management system for Outlook that uses AI to analyze, prioritize, categorize, and draft responses with minimal user intervention.

## Project Overview
This project connects to Microsoft Outlook via Microsoft Graph API and uses Claude to classify intent, prioritize messages, and generate safe, reviewable drafts. The system aims to reduce inbox load while keeping users in control.

## Folder Structure
- config/ — configuration and environment scaffolding
- docs/ — documentation and diagrams
- src/ — application source (to be implemented)
- tests/ — test suites

## Features Roadmap
- MVP
  - Connect to Outlook (Graph API), read inbox, basic categorization
  - Manual approval workflow and logging
- AI Integration
  - Intent/priority/sentiment/risk analysis
  - Draft response generation with constraints
- Automation & Learning
  - Confidence thresholds for auto-actions
  - Feedback loop to learn from user corrections
- Production Hardening
  - Robust error handling, observability, security hardening, CI/CD

## Setup Instructions (Placeholder)
- Install Python 3.11+
- Configure Microsoft Graph credentials and Claude API key
- Create and populate .env (see forthcoming .env.example)
- Install dependencies and run initial setup scripts

## Dependencies
- Microsoft Graph API (msal, httpx/requests)
- Anthropic Claude API client
- Python toolchain: pytest, pydantic, loguru/structlog, typer/click, asyncio, tenacity
- CI: GitHub Actions

## Security Notes
- Use least-privilege OAuth scopes (Mail.Read, Mail.ReadWrite, Mail.Send as required)
- Store secrets outside the repo; prefer Key Vault/secret manager in production
- Encrypt sensitive data at rest and in transit; minimize PII storage
- Validate AI outputs and sanitize prompts to prevent prompt injection

## Status
Scaffold and documentation committed. Application logic not yet implemented.

# Wayfair Market Intelligence Agent System

An end-to-end AI agent system built with n8n that automates market trend discovery, 
competitor monitoring, content generation, and executive dashboard creation for 
Wayfair's Rugs category.

## Overview

This project was built as part of the Wayfair AI Agent Engineering for Business 
Intelligence Externship through Extern. It consists of five interconnected AI agents 
that transform raw competitor and market data into actionable business intelligence.

## Agents

### Project 2 — Market Trend Discovery Agent
Scrapes Amazon product listings, pulls trend signals from blogs and social media, 
and uses AI to identify emerging style micro-segments with moodboard-style images.

### Project 3 — Competitor Monitoring Agent
Benchmarks Wayfair against Amazon and Walmart by scraping real product data, 
comparing pricing and assortment, and identifying whitespace opportunities.

### Project 4 — AI Content Generator
Takes insights from Projects 2 and 3 and generates tailored marketing content 
including blog ideas, social captions, email subject lines, and campaign concepts 
targeted to specific audiences and seasons.

### Project 5 — Market Intelligence Dashboard
Automatically pulls the latest P2 and P3 reports from Google Drive, parses them 
using Cheerio, and assembles a unified executive HTML dashboard with trend data, 
competitive analysis, pricing insights, and strategic recommendations.

## Tech Stack

- **n8n** — workflow automation and agent orchestration
- **Google Gemini** — AI content generation and analysis
- **Mistral** — product classification and trend identification
- **HuggingFace FLUX** — AI moodboard image generation
- **Cheerio** — HTML parsing and data extraction
- **Google Drive API** — report storage and retrieval
- **Docker** — local n8n deployment

## How It Works

1. A chat message triggers the workflow with a rug category and product URLs
2. The agent scrapes Amazon and Walmart for real product data
3. Social and blog signals are collected for trend context
4. AI agents classify, standardize, and analyze the data
5. Reports are generated as styled HTML files and uploaded to Google Drive
6. The dashboard agent pulls the latest reports and assembles a unified view

## Project Structure
wayfair-market-intelligence-agents/
├── workflows/
│   ├── P2_Market_Trend_Discovery.json
│   ├── P3_Competitor_Monitoring.json
│   ├── P4_AI_Content_Generator.json
│   └── P5_Dashboard_Builder.json
├── reports/
│   ├── P2_Market_Report_Area_Rug.html
│   ├── P3_Competitor_Report_Area_Rug.html
│   └── dashboard_template.html
└── README.md

## Sample Output

The system produces:
- Trend reports with AI-identified micro-segments and moodboard images
- Competitor analysis with pricing gaps and whitespace opportunities
- Tailored marketing content for specific audiences and seasons
- A unified executive dashboard combining all insights

## Setup

1. Install Docker Desktop and run n8n locally
2. Import workflow JSON files into n8n
3. Configure API credentials: Google Gemini, Mistral, HuggingFace, Google Drive OAuth
4. Create a "Wayfair Reports" folder in Google Drive
5. Trigger workflows via the n8n chat interface

## Built With

This project was developed during the Wayfair AI Agent Engineering for Business 
Intelligence Externship (April - July 2026) through Extern.

# Agentic AI Workflow: Business Lead Generation Assistant

This repository contains an **Agentic AI-powered automation workflow** built with [n8n](https://n8n.io/) to streamline the process of **business lead generation** using **Google Maps** and **Apify Website Content Crawler**. It intelligently automates the discovery, enrichment, and aggregation of potential business leads into a structured format for outreach, CRM integration, or analysis.

---

## 🎯 Use Case

Automate lead generation by:
- Extracting business listings based on a user query (e.g., “Find salons in Chicago”).
- Scraping and analyzing website content for each business.
- Aggregating and saving all enriched data into Google Sheets.
- Enabling immediate use for marketing, outreach, or analysis.

---

## ⚙️ Workflow Architecture

### 1. AI-Powered Lead Collection Trigger
- **Trigger**: Initiated via form/chatbot submission or webhook.
- **AI Agent**: Parses user query with GPT models and memory tools.
- **Google Fallback**: Optionally fetches data from web search if Maps data is sparse.

### 2. Google Maps Extractor Subworkflow
- Calls Apify's **Google Maps Scraper**.
- Extracts business names, locations, and contacts.
- Saves structured data to **Google Sheets**.

### 3. Website Content Crawler Subworkflow
- Uses URLs from Maps listings.
- Crawls sites via Apify **Website Content Crawler**.
- Extracts services, keywords, contact info.
- Appends results to the same **Google Sheet**.

---

## ✅ Expected Output

For each query:
- 📍 Location-based business listings are fetched.
- 🌐 Each business's website is scraped for detailed content.
- 📊 All data is saved in Google Sheets as a consolidated business profile.

---

## 🛠 Technologies & Tools

- [n8n.io](https://n8n.io/) – Low-code automation
- [Apify Google Maps Scraper](https://apify.com/apify/google-maps-scraper)
- [Apify Website Content Crawler](https://apify.com/apify/website-content-crawler)
- [OpenAI / GPT-Js](https://platform.openai.com/)
- Google Sheets API

---

## 📁 Repository Structure



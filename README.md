# Ads Performance & AI Diagnostic Tool

An automated internal tool built with **n8n** that monitors Google Ads campaigns, analyzes performance metrics using **OpenAI (GPT-4o)**, and delivers diagnostic reports via **Gmail**.

## 🚀 Overview
This project automates the tedious task of manual report cross-referencing. It identifies performance bottlenecks (such as low CTR or high CPC) and generates actionable insights to optimize bidding strategies and ad quality.

## 🛠️ System Architecture
- **Orchestrator:** [n8n](https://n8n.io/)
- **Data Source:** Google Ads API (Campaign & Search Term reports)
- **AI Engine:** OpenAI GPT-4o
- **Delivery:** Gmail (HTML Reports)

## 🔄 Workflow Logic
1.  **Schedule Trigger:** Runs automatically on a weekly basis.
2.  **Data Retrieval:** - Fetches active campaign metrics (Impressions, Clicks, CTR, Average CPC).
    - Retrieves the top 20 search terms from the last 7 days.
3.  **Data Transformation:** Formats raw metrics and search terms into a structured string for AI processing.
4.  **AI Analysis:** A specialized AI agent (Senior Google Ads Specialist) analyzes the data to identify why ads might be underperforming.
5.  **Reporting:** Generates a professional HTML report and sends it to the manager's email.

## 📦 Installation & Setup
1.  **n8n:** Import the provided workflow JSON file into your n8n instance.
2.  **Credentials:**
    - Configure **OAuth2** for the Google Ads node (Developer Token, Client ID, and Client Secret required).
    - Add your **OpenAI API Key**.
    - Configure the **Gmail** node for sending reports.
3.  **Customer IDs:** Set your `Manager Customer ID` and `Client Customer ID` in the Google Ads nodes.

## 🛡️ Security
This tool is for **internal use only**. All API interactions are secured via OAuth2, and diagnostic reports are sent to authorized internal emails.

---
*Developed to enhance digital marketing efficiency through data automation.*

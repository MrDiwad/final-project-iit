# 🚀 Automated Finance Briefing

An n8n workflow designed to automate the daily routine of checking financial news. Instead of manual scrolling through multiple websites, a curated summary is delivered directly to Telegram every morning at **8:01 AM**. ☕

### 🧐 How it works

1. **Data Collection**: Latest news is fetched from **Bankier.pl** and **Yahoo Finance**.
2. **Currency Tracking**: Current exchange rates (USD/EUR to PLN) are retrieved via the **NBP API**.
3. **AI Processing**: Data is passed to **Llama 3.1 (via Groq)**. The most relevant stories are selected, translated into English, and summarized using a casual, concise tone.
4. **Notification**: A formatted message is automatically sent to a designated **Telegram** chat.

### 🛠 Tech Stack

* **n8n**: Workflow automation platform.
* **Groq Cloud (Llama 3.1)**: Large Language Model for summarization and translation.
* **Telegram Bot API**: Messaging interface.
* **NBP API**: Source for currency exchange data.

### ⚙ Configuration

1. **Import**: The provided `.json` file is imported into an n8n instance.
2. **Credentials**: Connection is required for:
    * Groq API (for the LLM node).
    * Telegram Bot (Token and Chat ID).
3. **Scheduling**: The `Schedule Trigger` is set to 8:01 AM by default, though it can be adjusted to any preferred time.
4. **Execution**: Once the workflow is activated, the process runs autonomously.

# Credentials Required

All credentials are configured inside n8n under **Settings > Credentials**. Never hardcode API keys in the workflow JSON.

---

## 1. Groq API

Used for: AI content generation (LLaMA 3.3 70B)

| Field | Value |
|---|---|
| Credential Type | HTTP Header Auth |
| Header Name | `Authorization` |
| Header Value | `Bearer YOUR_GROQ_API_KEY` |

Get your key: https://console.groq.com/keys

---

## 2. Tavily API

Used for: Web search / real-time news fetching

| Field | Value |
|---|---|
| Credential Type | HTTP Header Auth |
| Header Name | `Authorization` |
| Header Value | `Bearer YOUR_TAVILY_API_KEY` |

Get your key: https://app.tavily.com

---

## 3. Brevo (Sendinblue) API

Used for: Sending email digests / notifications

| Field | Value |
|---|---|
| Credential Type | HTTP Header Auth |
| Header Name | `api-key` |
| Header Value | `YOUR_BREVO_API_KEY` |
| Sender Email | The verified sender email address from your Brevo account |

Get your key: https://app.brevo.com/settings/keys/api

---

## 4. Telegram Bot

Used for: Sending posts/alerts via Telegram

| Field | Value |
|---|---|
| Credential Type | Telegram API |
| Bot Token | `YOUR_TELEGRAM_BOT_TOKEN` |
| Chat ID | Your personal or group Chat ID |

Setup steps:
1. Message `@BotFather` on Telegram → `/newbot`
2. Copy the token provided
3. Get your Chat ID by messaging `@userinfobot`

---

## 5. Notion API

Used for: Saving generated posts to a Notion database

| Field | Value |
|---|---|
| Credential Type | Notion API |
| API Key | `YOUR_NOTION_API_KEY` (Internal Integration Token) |
| Database ID | The ID from your Notion database URL |

Setup steps:
1. Go to https://www.notion.so/my-integrations → Create integration
2. Copy the Internal Integration Token
3. Open your Notion database → Share → Invite your integration
4. Copy the Database ID from the URL: `notion.so/YOUR_DATABASE_ID?v=...`

---

## Quick Reference

```
GROQ_API_KEY=your_groq_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here
BREVO_API_KEY=your_brevo_api_key_here
BREVO_SENDER_EMAIL=your_verified_sender@email.com
TELEGRAM_BOT_TOKEN=your_telegram_bot_token_here
TELEGRAM_CHAT_ID=your_chat_id_here
NOTION_API_KEY=your_notion_integration_token_here
NOTION_DATABASE_ID=your_notion_database_id_here
```

All of the above are entered directly into n8n's credential manager — no `.env` file is needed when running on n8n Cloud or self-hosted n8n.

# Credentials Required

This n8n workflow requires the following credentials to be configured before importing.

## 1. OpenAI API

| Field | Value |
|---|---|
| Credential Type | OpenAI API |
| API Key | Your OpenAI API key |

Get your key at: [platform.openai.com/api-keys](https://platform.openai.com/api-keys)

## 2. LinkedIn OAuth2

| Field | Value |
|---|---|
| Credential Type | LinkedIn OAuth2 API |
| Client ID | From LinkedIn Developer App |
| Client Secret | From LinkedIn Developer App |
| Scope | `w_member_social`, `r_liteprofile` |

Setup steps:
1. Go to [LinkedIn Developer Portal](https://www.linkedin.com/developers/)
2. Create a new app
3. Under "Products", request access to **Share on LinkedIn**
4. Copy Client ID and Client Secret into n8n

## 3. (Optional) Google Sheets

Only required if you use Google Sheets as your content source node.

| Field | Value |
|---|---|
| Credential Type | Google Sheets OAuth2 API |
| Authentication | OAuth2 |

## How to Add Credentials in n8n

1. Open n8n and go to **Settings > Credentials**
2. Click **Add Credential**
3. Search for the credential type and fill in the fields above
4. Import the workflow JSON (`Automated LinkedIn Post Creator.json`)
5. Open each node that shows a credential warning and select the matching credential

## Notes

- The workflow does not store any API keys in the JSON file
- Never commit real API keys or tokens to this repository
- Use n8n's built-in credential manager for all secrets

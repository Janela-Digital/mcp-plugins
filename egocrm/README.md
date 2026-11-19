# eGO CRM for Claude

Connect Claude to eGO CRM to look up your properties, contacts, leads, visits,
tasks, and notes using natural language. The connection provides read-only
access to eGO records.

## What’s included

- **MCP connector `ego-crm`** — a remote server at `https://api.egocrm.com/mcp/`
  that uses your eGO account for authentication (OAuth 2.0 with PKCE). Claude
  never sees your password.
- **eGO CRM lookup skill** — guides Claude in using eGO tools, handling
  pagination, and answering in business terms.

## Getting started

1. Install the **eGO CRM** plugin.
2. Open the plugin’s **Connectors** tab and click **Connect** next to `ego-crm`.
   If a setup screen appears, click **Add** with the default settings.
3. Sign in with your eGO account and choose your agency.
4. Try asking “What visits do I have scheduled this week?”

For Claude Team or Enterprise accounts, the organization owner installs the
plugin and adds the connector once. Each user signs in to eGO as described in
step 3 and can then start asking questions.

If your session expires, reconnect using the same steps.

## Requirements

- An eGO CRM account with access to the application.
- Claude.ai or the Claude Desktop app with plugins enabled.

## Support

For account questions, training, or technical help, contact official eGO support.

## Privacy and terms

The data you access is handled according to the [eGO Privacy Policy](https://www.egocrm.com/privacy-policy).

See the [eGO Terms and Conditions](https://www.egocrm.com/terms-conditions) for the terms of use.

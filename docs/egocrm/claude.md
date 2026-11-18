---
title: eGO CRM for Claude
permalink: /egocrm/claude/
connector: egocrm
platform: claude
---

# eGO CRM for Claude

<nav class="page-toc" aria-label="On this page">
<strong>On this page</strong>
<ol>
<li><a href="#about">About</a></li>
<li><a href="#availability">Availability and languages</a></li>
<li><a href="#getting-started">How to get started</a></li>
<li><a href="#capabilities">What you can do</a></li>
<li><a href="#results">How results are displayed</a></li>
<li><a href="#examples">Usage examples</a></li>
<li><a href="#tools">Available tools</a></li>
<li><a href="#permissions">Authentication, data and limitations</a></li>
<li><a href="#support">Support and policies</a></li>
</ol>
</nav>

## 1. About
{: #about }

Connect Claude to eGO CRM to search and read your agency's properties, contacts, leads, visits, tasks and notes in natural language. This connector is for real estate professionals with an eGO account. It is read-only: it cannot create, change or delete CRM records.

## 2. Availability and languages
{: #availability }

- **Access:** real estate professionals with an eGO account and agency access.
- **Data:** only records permitted by the signed-in account.
- **Documentation:** available in English.
- **App:** connector availability depends on your account and organization policies.

You can write requests in natural language. The language of this documentation does not change the language settings of Claude or ChatGPT.

## 3. How to get started
{: #getting-started }

1. Install the **eGO CRM** plugin from the [plugin directory](https://claude.ai/plugins).
2. Open **Connectors** and connect **ego-crm**.
3. Sign in to eGO and select your agency.
4. Write your request in natural language; you do not need to know tool names.

## 4. What you can do
{: #capabilities }

- Search properties, contacts, opportunities and leads.
- Read details of a selected record.
- Review related visits, contacts, properties and interested leads.
- Consult tasks, assigned users, dates and notes.
- Get official eGO product, training and support guidance.

## 5. How results are displayed
{: #results }

Results are presented as summaries or lists with relevant information such as reference, name, price, status or dates. Ask for a record's details or relationships without repeating every search criterion.

When more pages are available, ask for the next results. Names and references identify records in the conversation; technical selections are handled internally by the connector.

## 6. Usage examples
{: #examples }

### 1. Search properties and relationships

**Request**

> Show my three-bedroom properties for sale and who has visited them.

**Expected result**

The assistant searches properties and reads visits for selected results, subject to your account permissions.

**Follow-up:** "Show details of the second property."

### 2. Review leads

**Request**

> Show unread leads without an assigned owner created this month.

**Expected result**

A paginated list of leads matching the filters, without changing records.

**Follow-up:** "What is the first lead looking for?"

### 3. Review tasks and notes

**Request**

> What tasks are assigned to me this week?

**Expected result**

Tasks assigned to you for the requested period. Notes are retrieved for a selected task.

**Follow-up:** "Show the notes on the first task."

### 4. Request a change

**Request**

> Change this property price to EUR 300,000.

**Expected result**

The assistant explains that the connection is read-only and the change must be made in eGO.

## 7. Available tools
{: #tools }

Search first, then request details or related records for a selected result. You can refer to a record by its name, reference or position in the results.

| Tool | Purpose |
| --- | --- |
| `find_contacts` | Search contacts. |
| `find_leads` | Search opportunities and leads. |
| `find_properties` | Search properties and show a summary with reference, title and price. |
| `get_contact` | Get the current details of a selected contact. |
| `get_ego_guidance` | Get official eGO information about the product, CRM capabilities, account access, training and support. |
| `get_lead` | Get the current details of a selected lead. |
| `get_mcp_guidance` | Explain what eGO CRM can do in this assistant and how to get started. |
| `get_note` | Get the details of a selected note. |
| `get_property` | Get the full details of a selected property. |
| `get_task` | Get the current details of a selected task. |
| `list_contact_properties` | List the properties linked to a selected contact. |
| `list_lead_contacts` | List the contacts linked to a selected lead. |
| `list_lead_preferences` | List the preferences of a selected lead. |
| `list_lead_properties` | List the properties linked to a selected lead. |
| `list_lead_tasks` | List the tasks linked to a selected lead. |
| `list_notes` | List the notes of a selected record. |
| `list_property_contacts` | List the contacts linked to a selected property. |
| `list_property_interested_leads` | List the leads interested in a selected property. |
| `list_property_tasks` | List the tasks linked to a selected property. |
| `list_property_visit_tasks` | List the viewing tasks linked to a selected property. |
| `list_property_visits` | List the viewings recorded for a selected property. |
| `list_tasks` | Search tasks. |

## 8. Authentication, data and limitations
{: #permissions }

### Authentication and permissions

Sign in to eGO through the authorization screen and select your agency. Authentication uses OAuth 2.0 authorization code flow with PKCE (S256). Never paste a password, authorization code or access token into the conversation. If the session expires, reconnect through the app.

| Scope | Purpose |
| --- | --- |
| `ego:api` | Authorize access to the eGO API for the signed-in account; the tools exposed by this connector are read-only. |
| `offline_access` | Allow the app to refresh authorization without repeated sign-in. |

The authorization screen shows the requested permissions. Your agency access and account permissions determine which records you can consult.

### Connector configuration

Use the eGO CRM plugin and connect its `ego-crm` connector. The plugin is available in the [plugin directory](https://claude.ai/plugins) and configures the OAuth client ID `claude`. The remote MCP endpoint is `https://api.egocrm.com/mcp/`.

### Data used

Search requests send the criteria you provide, such as names, references, locations, dates, statuses or contact details, to eGO. Follow-up requests identify a selected CRM record and the relationship or detail you want to read.

Responses may contain personal and business information, including names, email addresses, telephone numbers, property data, lead preferences, visit details, task assignments and notes. Returned information becomes available to Claude in the conversation. Request only information needed for your work and follow your agency's rules for sharing CRM data with an assistant.

This connector does not send messages to contacts or update CRM records. Review the eGO privacy policy and your Claude account or workspace data settings before connecting.

### Limitations

All CRM access through this connector is read-only. Create or update properties, contacts, leads, visits, tasks and notes directly in eGO. The connector cannot send messages, reset passwords, change accounts or book training.

Results are paginated. Ask for the next page when more results are available; a single page should not be treated as a complete list. Notes belong to a selected property, contact, lead or task; global note search is not supported. If a selected result expires, repeat the original search.

The connector reports the records returned by eGO; it does not independently verify their completeness or accuracy. An empty result means no records matched the criteria and permissions used. A failed lookup should be reported rather than replaced with an assumed result.

## 9. Support and policies
{: #support }

- [eGO CRM website](https://www.egocrm.com/)
- [Support and contact](https://www.egocrm.com/contact-us)
- [Privacy policy](https://www.egocrm.com/privacy-policy)
- [Terms and conditions](https://www.egocrm.com/terms-conditions)

Use official eGO support for account access, training or service issues. For connection or workspace permission issues, contact your Claude administrator or Claude support.

---
title: CasaSAPO for Claude
permalink: /casasapo/claude/
connector: casasapo
platform: claude
---

# CasaSAPO for Claude

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

CasaSAPO helps you find properties for sale, rent or holiday rentals in Portugal, view listing details, contact advertisers and create property alerts from a conversation in Claude.

## 2. Availability and languages
{: #availability }

- **Property location:** Portugal.
- **Account:** not required for public search; required to contact advertisers and create alerts.
- **Documentation:** available in English.
- **App:** connector availability depends on your account and organization policies.

You can write requests in natural language. The language of this documentation does not change the language settings of Claude or ChatGPT.

## 3. How to get started
{: #getting-started }

1. Install the **CasaSAPO** plugin from the [plugin directory](https://claude.ai/plugins).
2. Enable the plugin or its MCP connection in Claude, according to your account permissions.
3. Specify the operation, location and property category.
4. To contact advertisers or create alerts, follow the sign-in steps shown by Claude.

## 4. What you can do
{: #capabilities }

- Search properties for sale, rent or holiday rentals by location and filters.
- Refine a search with new criteria.
- Read details and features of a returned listing.
- Contact the advertiser of a selected property.
- Create alerts using your authenticated account.
- Get portal, account and support guidance.

## 5. How results are displayed
{: #results }

Returned listings can be presented in a property-card carousel. When interactive cards are unavailable, use the returned listing links in the text response.

Cards and responses use titles, prices, features and links returned by the service. Open a listing link to continue on the portal.

Specify the operation, location and property category. Locations are resolved by district, municipality, parish and zone; if several locations match, choose one of the returned options.

## 6. Usage examples
{: #examples }

### 1. Search and refine

**Request**

> Find two-bedroom apartments for sale in Lisbon under EUR 350,000.

**Expected result**

Listings matching your criteria, with the information and links returned by the portal. If no listings match, the assistant reports an empty search result.

**Follow-up:** "Show only those with a pool."

### 2. Read listing details

**Request**

> Show details of the second property in those results.

**Expected result**

Available details of the selected listing, without inventing features or availability.

**Follow-up:** "Which areas and features are listed?"

### 3. Contact an advertiser

**Request**

> I want to contact the advertiser of this listing to ask about a viewing.

**Expected result**

The assistant uses the selected listing and your authenticated account to send the enquiry. An explicit contact request authorizes this action. It reports success only when the service confirms it.

### 4. Create an alert

**Request**

> Create an alert for this search.

**Expected result**

The assistant confirms the criteria and uses your authenticated account. It reports completion only after the service confirms creation.

### 5. Clarify a location

**Request**

> Find apartments to rent near me.

**Expected result**

The assistant asks for a concrete location. If the service returns several possible locations, it offers those options for selection before continuing.

## 7. Available tools
{: #tools }

| Tool | Purpose |
| --- | --- |
| `search` | Search property listings in Portugal by operation, location, category and filters. |
| `detail` | Read a selected listing using its returned listingId and systemId, reference or unique identifier. |
| `get_search_context` | Read supported operations, property categories, features and pagination limits. |
| `get_mcp_guidance` | Explain the connector's capabilities and how to get started. |
| `get_casasapo_guidance` | Read official portal, account, rental-safety and support guidance. |
| `render_listings_widget` | Present returned listings as a property-card carousel in a compatible app. |
| `submit_lead` | Send an enquiry to the selected listing's advertiser using the authenticated account. |
| `create_alert` | Create a saved-search alert or a 10% price-change alert for one listing using the authenticated account. |

## 8. Authentication, data and limitations
{: #permissions }

### Authentication and permissions

Public search, listing details and guidance do not require a portal login. Contacting an advertiser and creating an alert require your CasaSAPO account through OAuth 2.0.

| Scope | Purpose |
| --- | --- |
| `property-interest:write` | Authorize advertiser-contact requests and property alerts. |
| `offline_access` | Allow the app to refresh authorization without asking you to sign in for each request. |

The authorization screen shows the permissions requested by the app. Sign in there, never in the conversation. Contact and alert tools use the account's name, email and phone internally; the assistant should not ask you to type those details into chat.

An explicit request to contact a selected advertiser authorizes that contact request. Confirm the criteria before creating an alert. Wait for the service's confirmation before treating the action as complete. If the outcome is uncertain, check before repeating it to avoid duplicates.

### Connector configuration

Use the CasaSAPO plugin or configure its remote MCP connector in Claude. The plugin is available in the [plugin directory](https://claude.ai/plugins). The MCP endpoint is `https://casa.sapo.pt/mcp`. Follow the app's connection steps and sign in to CasaSAPO when an action requires authorization. If authorization expires, reconnect through the app.

### Data used

Searches send your location, operation, property category and requested filters to CasaSAPO. Listing lookups send the selected listing's identifiers. Results may include advertiser-provided descriptions, prices, locations, features, photographs and public listing links; these become available to the assistant.

Contact requests use your authenticated account's contact details, the selected listing and any approved message. Alerts use your account and the selected search or listing. Do not include unrelated personal information in search text or messages.

### Limitations

The connector searches listings in Portugal. It does not independently verify advertisers, property condition, legal status or availability. Results and prices reflect the information returned by the service at the time of the request. Search results are paginated; one page is not necessarily the full result set.

It does not publish or edit adverts, make payments, change account settings or complete a property transaction. A contact request is an enquiry, not a confirmed viewing or reservation. Complete unsupported actions on the portal. If no results match or a request fails, the assistant should report that outcome and must not make up listings or results.

## 9. Support and policies
{: #support }

- [CasaSAPO website](https://casa.sapo.pt)
- [Support and contact](https://casa.sapo.pt/general/contacto.aspx)
- [Privacy policy](https://casa.sapo.pt/politica-de-privacidade)
- [Terms of use](https://casa.sapo.pt/general/condicoes/condicoes_portal.aspx)

For account or service issues, use the official support link. For connection or workspace permission issues, contact your Claude administrator or Claude support.

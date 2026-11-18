---
title: SUPERCASA for Claude
permalink: /supercasa/claude/
connector: supercasa
platform: claude
---

# SUPERCASA for Claude

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

SUPERCASA helps you find properties for sale, rent or holiday rentals in Portugal, view listing details, contact advertisers and create property alerts from a conversation in Claude.

## 2. Availability and languages
{: #availability }

- **Property location:** Portugal.
- **Account:** not required for public search; required to contact advertisers and create alerts.
- **Documentation:** available in English.
- **App:** connector availability depends on your account and organization policies.

You can write requests in natural language. The language of this documentation does not change the language settings of Claude.

## 3. How to get started
{: #getting-started }

1. Open **SUPERCASA** from your installed plugins in Claude. The [plugin directory](https://claude.ai/plugins){:target="_blank" rel="noopener"} is the starting point for finding plugins available to your account.
2. On the plugin page, find the **Connectors** section and select **Connect** next to **SUPERCASA**.
3. Follow the SUPERCASA sign-in and authorization flow, review the requested permissions and select **Authorize**.
4. Return to your Claude conversation and ask for what you need, naming SUPERCASA in your request if necessary.

You do not need to call tools or provide technical identifiers. The screenshots show a custom-connector setup in Claude; connector names and available options can vary with your workspace.

<figure>
  <a href="{{ '/assets/images/supercasa/claude/connector-setup.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/claude/connector-setup.png' | relative_url }}" alt="The SUPERCASA connector page in Claude, showing the Connect button, connection status and authorization requirement." loading="lazy"></a>
  <figcaption>The SUPERCASA connector page in Claude, showing the Connect button, connection status and authorization requirement.</figcaption>
</figure>

The illustrated Claude connector is labelled **Sign-in required**, so its connection flow can ask you to authorize access before your first search. Public search tools do not require portal authentication at server level; contacting advertisers and creating alerts require your account authorization.

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

Claude displays the connector activity in the conversation and can show an interactive property carousel inside a tool result. The SUPERCASA example below shows the **search_properties** result, followed by Claude's written summary.

<figure>
  <a href="{{ '/assets/images/supercasa/claude/search-results.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/claude/search-results.png' | relative_url }}" alt="SUPERCASA search results inside Claude, with property cards, listing links and a written summary below the tool result." loading="lazy"></a>
  <figcaption>SUPERCASA search results inside Claude, with property cards, listing links and a written summary below the tool result.</figcaption>
</figure>

Use the listing buttons to continue to the portal, or ask Claude about a particular result, such as the second property. Claude uses returned listing identifiers internally to read its details; you do not need to copy tool parameters into the conversation.

If interactive cards are unavailable, Claude can present the returned listing information and links in text. Card labels and advertiser descriptions may remain in the language returned by the service even when your conversation is in English. Screenshots illustrate one search; their prices and counts are not current availability guarantees.

Specify the operation, location and property category. If the location is ambiguous, Claude presents the returned options and continues after you select one. A normal SUPERCASA search already provides its results widget; the separate rendering tool is for an explicitly requested subset.

## 6. Usage examples
{: #examples }

### 1. Search and refine in Claude

**Request**

> Using SUPERCASA, show me five apartments in the Lisbon district to buy.

**How Claude responds**

Claude searches SUPERCASA, presents returned listings in a carousel when supported and follows with a written summary and listing links. The screenshot above illustrates this flow. If no listings match, Claude reports an empty result rather than inventing properties.

**Follow-up:** "Narrow this search to two bedrooms and a maximum price of EUR 350,000."

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

Claude uses the selected listing and your authenticated account to send the enquiry. It sends the enquiry only when you clearly ask to contact the advertiser. It reports success only when the service confirms it.

### 4. Create an alert

**Request**

> Create an alert for this search.

**Expected result**

Claude confirms the criteria and uses your authenticated account. It reports completion only after the service confirms creation.

### 5. Clarify a location

**Request**

> Find apartments to rent near me.

**Expected result**

Claude asks for a concrete location. If the service returns several possible locations, it offers those options for selection before continuing.

## 7. Available tools
{: #tools }

| Tool | Purpose |
| --- | --- |
| `search_properties` | Search Portugal listings and developments and show the results as property cards. |
| `get_property_details` | Read advertiser-published details for a selected listing ID or reference. |
| `get_search_context` | Read supported operations, categories, search profiles, filters and pagination limits. |
| `get_mcp_guidance` | Explain the connector's capabilities and how to get started. |
| `get_supercasa_guidance` | Read official portal, account, rental-safety and support guidance. |
| `render_listings_widget` | Show or compare selected listings from earlier results, when you ask. |
| `submit_lead` | Send an enquiry to the selected listing's advertiser using the authenticated account. |
| `create_alert` | Create a search alert, or an alert for similar properties based on one selected listing. |

## 8. Authentication, data and limitations
{: #permissions }

### Authentication and permissions

Public search, listing details and guidance do not require a portal login. Contacting an advertiser and creating an alert require your SUPERCASA account through OAuth 2.0.

| Scope | Purpose |
| --- | --- |
| `property-interest:write` | Authorize advertiser-contact requests and property alerts. |
| `offline_access` | Allow the app to refresh authorization without asking you to sign in for each request. |

The authorization screen shows the permissions requested by the app. Sign in there, never in the conversation. Contact and alert tools use the account's name, email and phone internally; Claude should not ask you to type those details into chat.

Claude contacts an advertiser only when you clearly ask for it, and confirms the criteria before creating an alert. Signing in alone does not request an action. Wait for the service's confirmation before treating the action as complete. If the outcome is uncertain, check before repeating it to avoid duplicates.

<figure>
  <a href="{{ '/assets/images/supercasa/claude/authorization.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/claude/authorization.png' | relative_url }}" alt="SUPERCASA authorization screen requested by Claude, for advertiser contact, property alerts and connection renewal." loading="lazy"></a>
  <figcaption>SUPERCASA authorization screen requested by Claude, for advertiser contact, property alerts and connection renewal.</figcaption>
</figure>

### Connector configuration

Use the SUPERCASA plugin or configure its remote MCP connector in Claude. The plugin is available in the [plugin directory](https://claude.ai/plugins){:target="_blank" rel="noopener"}. The MCP endpoint is `https://mcp.supercasa.pt/mcp`. Follow the app's connection steps and sign in to SUPERCASA when an action requires authorization. If authorization expires, reconnect through the app.

### Data used

Searches send your location, operation, property category and requested filters to SUPERCASA. Listing lookups send the selected listing's identifiers. Results may include advertiser-provided descriptions, prices, locations, features, photographs and public listing links; these become available to Claude.

Contact requests use your authenticated account's contact details, the selected listing and any approved message. Alerts use your account and the selected search or listing. Do not include unrelated personal information in search text or messages.

### Limitations

The connector searches listings in Portugal. It does not independently verify advertisers, property condition, legal status or availability. Results and prices reflect the information returned by the service at the time of the request. Search results are paginated; one page is not necessarily the full result set.

It does not publish or edit adverts, make payments, change account settings or complete a property transaction. A contact request is an enquiry, not a confirmed viewing or reservation. Complete unsupported actions on the portal. If no results match or a request fails, Claude should report that outcome and must not make up listings or results.

## 9. Support and policies
{: #support }

- [SUPERCASA website](https://supercasa.pt){:target="_blank" rel="noopener"}
- [Support and contact](https://supercasa.pt/en-gb/contactos){:target="_blank" rel="noopener"}
- [Privacy policy](https://supercasa.pt/en-gb/politica-privacidade){:target="_blank" rel="noopener"}
- [Terms of use](https://supercasa.pt/en-gb/condicoes-utilizacao){:target="_blank" rel="noopener"}

For account or service issues, use the official support link. For connection or workspace permission issues, contact your Claude administrator or Claude support.

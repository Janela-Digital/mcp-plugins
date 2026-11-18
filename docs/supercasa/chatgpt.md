---
title: SUPERCASA for ChatGPT
permalink: /supercasa/chatgpt/
connector: supercasa
platform: chatgpt
---

# SUPERCASA for ChatGPT

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

SUPERCASA helps you find properties for sale, rent or holiday rentals in Portugal, view listing details, contact advertisers and create property alerts from a conversation in ChatGPT.

## 2. Availability and languages
{: #availability }

- **Property location:** Portugal.
- **Account:** not required for public search; required to contact advertisers and create alerts.
- **Documentation:** available in English.
- **App:** connector availability depends on your account and organization policies.

You can write requests in natural language. The language of this documentation does not change the language settings of ChatGPT.

## 3. How to get started
{: #getting-started }

1. Open the **SUPERCASA** plugin page in the [plugin directory](https://chatgpt.com/plugins){:target="_blank" rel="noopener"}.
2. Select **Install plugin**, when that option is available.
3. Select the plugin in the conversation and write your request in natural language.
4. When requesting contact or an alert, sign in to SUPERCASA and review the requested authorization.

The screenshots below show the interface used for these examples; labels may vary with your app version.

<figure>
  <a href="{{ '/assets/images/supercasa/chatgpt/plugin-overview.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/chatgpt/plugin-overview.png' | relative_url }}" alt="The SUPERCASA plugin page, with the installation option and suggested prompts." loading="lazy"></a>
  <figcaption>The SUPERCASA plugin page, with the installation option and suggested prompts.</figcaption>
</figure>

<figure>
  <a href="{{ '/assets/images/supercasa/chatgpt/search-prompt.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/chatgpt/search-prompt.png' | relative_url }}" alt="An example request with the SUPERCASA plugin selected in the conversation." loading="lazy"></a>
  <figcaption>An example request with the SUPERCASA plugin selected in the conversation.</figcaption>
</figure>

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

Search results are shown as property cards. You can also ask to see or compare only some of the listings. When interactive cards are unavailable, use the returned listing links in the text response.

Cards and responses use titles, prices, features and links returned by the service. Open a listing link to continue on the portal. The example screenshot does not show current prices or availability.

Specify the operation, location and property category. If a place name is ambiguous, choose one of the returned locations, and the search continues with that location.

<figure>
  <a href="{{ '/assets/images/supercasa/chatgpt/search-results.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/chatgpt/search-results.png' | relative_url }}" alt="Example search for two-bedroom apartments in Lisbon, with a property carousel and a link to the SUPERCASA results." loading="lazy"></a>
  <figcaption>Example search for two-bedroom apartments in Lisbon, with a property carousel and a link to the SUPERCASA results.</figcaption>
</figure>

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

The assistant uses the selected listing and your authenticated account to send the enquiry. It sends the enquiry only when you clearly ask to contact the advertiser. It reports success only when the service confirms it.

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

The authorization screen shows the permissions requested by the app. Sign in there, never in the conversation. Contact and alert tools use the account's name, email and phone internally; the assistant should not ask you to type those details into chat.

The assistant contacts an advertiser only when you clearly ask for it, and confirms the criteria before creating an alert. Signing in alone does not request an action. Wait for the service's confirmation before treating the action as complete. If the outcome is uncertain, check before repeating it to avoid duplicates.

<figure>
  <a href="{{ '/assets/images/supercasa/chatgpt/authorization.png' | relative_url }}" target="_blank" rel="noopener"><img src="{{ '/assets/images/supercasa/chatgpt/authorization.png' | relative_url }}" alt="SUPERCASA authorization for contact requests and alerts, including connection renewal." loading="lazy"></a>
  <figcaption>SUPERCASA authorization for contact requests and alerts, including connection renewal.</figcaption>
</figure>

### Connector configuration

Use the SUPERCASA app or a configured remote MCP connection in ChatGPT, subject to availability and your workspace's settings. The MCP endpoint is `https://mcp.supercasa.pt/mcp`. Follow the app's connection steps and sign in to SUPERCASA when an action requires authorization. If authorization expires, reconnect through the app.

### Data used

Searches send your location, operation, property category and requested filters to SUPERCASA. Listing lookups send the selected listing's identifiers. Results may include advertiser-provided descriptions, prices, locations, features, photographs and public listing links; these become available to the assistant.

Contact requests use your authenticated account's contact details, the selected listing and any approved message. Alerts use your account and the selected search or listing. Do not include unrelated personal information in search text or messages.

### Limitations

The connector searches listings in Portugal. It does not independently verify advertisers, property condition, legal status or availability. Results and prices reflect the information returned by the service at the time of the request. Search results are paginated; one page is not necessarily the full result set.

It does not publish or edit adverts, make payments, change account settings or complete a property transaction. A contact request is an enquiry, not a confirmed viewing or reservation. Complete unsupported actions on the portal. If no results match or a request fails, the assistant should report that outcome and must not make up listings or results.

## 9. Support and policies
{: #support }

- [SUPERCASA website](https://supercasa.pt){:target="_blank" rel="noopener"}
- [Support and contact](https://supercasa.pt/en-gb/contactos){:target="_blank" rel="noopener"}
- [Privacy policy](https://supercasa.pt/en-gb/politica-privacidade){:target="_blank" rel="noopener"}
- [Terms of use](https://supercasa.pt/en-gb/condicoes-utilizacao){:target="_blank" rel="noopener"}

For account or service issues, use the official support link. For connection or workspace permission issues, contact your ChatGPT administrator or ChatGPT support.

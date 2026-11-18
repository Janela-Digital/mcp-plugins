---
title: Janela Digital MCP connectors
permalink: /
---

# Janela Digital MCP connectors

Use CasaSAPO, SUPERCASA and eGO CRM through Claude or ChatGPT. These pages describe each connector's capabilities, tools, authentication, data use and limits for users and workspace administrators.

| Connector | Intended audience | Claude | ChatGPT |
| --- | --- | --- | --- |
| CasaSAPO | People searching property listings in Portugal | [Documentation]({{ '/casasapo/claude/' | relative_url }}) | [Documentation]({{ '/casasapo/chatgpt/' | relative_url }}) |
| SUPERCASA | People searching property listings in Portugal | [Documentation]({{ '/supercasa/claude/' | relative_url }}) | [Documentation]({{ '/supercasa/chatgpt/' | relative_url }}) |
| eGO CRM | Real estate professionals with an eGO account | [Documentation]({{ '/egocrm/claude/' | relative_url }}) | [Documentation]({{ '/egocrm/chatgpt/' | relative_url }}) |

## Before connecting

CasaSAPO and SUPERCASA provide public listing searches and details. Contacting advertisers and creating alerts require an authenticated portal account and send information to the service. eGO CRM requires an authenticated account to access business records; its connector is read-only.

Sign in only through the service's authorization screen. Do not share passwords, authorization codes or access tokens in a conversation. Your organization's administrator may need to approve access. Availability depends on your assistant account and workspace settings.

Information returned by a connector becomes available to the assistant in the conversation. Review the relevant service's privacy policy and your assistant provider's data settings before using personal or business data.

## Support and policies
{: #support }

- **CasaSAPO:** [Support](https://casa.sapo.pt/general/contacto.aspx), [privacy](https://casa.sapo.pt/politica-de-privacidade), [terms](https://casa.sapo.pt/general/condicoes/condicoes_portal.aspx).
- **SUPERCASA:** [Support](https://supercasa.pt/contactos), [privacy](https://supercasa.pt/politica-privacidade), [terms](https://supercasa.pt/condicoes-utilizacao).
- **eGO CRM:** [Support](https://www.egocrm.com/contact-us), [privacy](https://www.egocrm.com/privacy-policy), [terms](https://www.egocrm.com/terms-conditions).

[Plugin source repository](https://github.com/Janela-Digital/mcp-plugins)

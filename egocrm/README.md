# eGO CRM para o Claude


## Install from the repository (Claude Code)

Repository: [Janela-Digital/mcp-plugins](https://github.com/Janela-Digital/mcp-plugins).

Run in Claude Code:

```text
/plugin install egocrm --marketplace Janela-Digital/mcp-plugins
```

Ligue o Claude ao eGO CRM e consulte, em linguagem natural, os seus imóveis,
contactos, leads, visitas, tarefas e notas. A ligação é apenas de leitura: o
Claude pesquisa e lê registos, mas não cria, altera nem apaga dados no eGO.

## O que inclui

- **Conector MCP `ego-crm`** — servidor remoto em `https://api.egocrm.com/mcp/`,
  autenticado com a sua conta eGO (OAuth 2.0 com PKCE). O Claude nunca vê a sua
  palavra-passe.
- **Skill `consultar-ego`** — orienta o Claude a usar as ferramentas do eGO,
  a respeitar a paginação e a responder em termos de negócio.

## Primeira utilização

1. Instale o plugin **eGO CRM**.
2. Abra o separador **Connectors** do plugin e clique em **Connect** no conector `ego-crm`.
   Se aparecer um ecrã de configuração, clique em **Add** sem alterar nada.
3. Inicie sessão com a sua conta eGO e escolha a agência.
4. Pergunte, por exemplo: *"Que visitas tenho marcadas esta semana?"*

Em contas Claude Team ou Enterprise, o Owner da organização instala o plugin e
adiciona o conector uma vez; cada utilizador só inicia sessão no eGO (passo 3) e
começa a perguntar.

Se a sessão expirar, volte a ligar o conector da mesma forma.

## Requisitos

- Conta eGO CRM com acesso à aplicação.
- claude.ai ou app Claude Desktop com plugins activos.

## Suporte

Para questões de conta, formação ou suporte, contacte o suporte oficial eGO.

## Privacidade

Os dados consultados são tratados segundo a
[Política de Privacidade do eGO](https://www.egocrm.com/privacy-policy).

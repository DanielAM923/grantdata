# Impact Recon (alpha)

Impact Recon is an early research tool for nonprofit, funding and research records. It connects to Claude or ChatGPT as a remote MCP server. Results may be incomplete or inaccurate, so check the linked evidence. The tools are read only; saving and graph edits are unavailable. Shared alpha usage limits may interrupt requests.

## Connection details

Name: **Impact Recon Alpha**

Remote MCP URL (paste the whole address into the connector field; it is not a web page):

```
https://emerald-mcp.redbeach-93eee11c.eastus.azurecontainerapps.io/mcp-public
```

Authentication: **No sign in**. No API key or cloud account is needed.

## Claude (claude.ai or the Desktop app)

Your own account:

1. Open **Customize → Connectors → Add custom connector**.
2. Enter the name and URL above, choose **No sign in**, and add it.
3. Start a new chat, open the tools menu, turn on **Impact Recon Alpha**, and ask the first prompt below.

A Free plan allows one custom connector; Pro and Max are not limited. The Desktop app uses the same connectors as claude.ai.

Work or university workspace: an owner or admin adds the connector once under the organization's **Settings → Connectors → Add custom connector**, then each member connects it under **Customize → Connectors**. If the option is missing, forward this page to the workspace's Claude administrator. No separate subscription is needed to try it.

Official steps: [Get started with custom connectors](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

## Claude Code

Tools plus the nine research guides as skills:

```bash
claude plugin marketplace add DanielAM923/impact-recon
claude plugin install impact-recon@impact-recon
```

Tools only:

```bash
claude mcp add --transport http --scope user impact-recon https://emerald-mcp.redbeach-93eee11c.eastus.azurecontainerapps.io/mcp-public
```

## ChatGPT

If your account offers custom MCP connections: open **Plugins**, select the plus button and **Add custom MCP server**, enter the name and URL above, choose authentication **None**, create the plugin, then mention **@Impact Recon Alpha** in a new conversation. If the option is absent, account or workspace permissions may block this route; upgrading is not a verified fix. See [OpenAI's connection instructions](https://developers.openai.com/plugins/deploy/connect-chatgpt).

## First prompt

> Use Impact Recon to tell me about Emerald South Economic Development Collaborative's observed funding. Give a short answer with the evidence dates and any important gaps. Distinguish historical funding from current opportunities.

For research:

> Use Impact Recon to find research on nonprofit service delivery. Separate directly relevant papers from adjacent work, and tell me whether the review used full text, a webpage, an abstract or metadata.

## What is in this repository

`plugins/impact-recon/` is a Claude Code plugin: the remote MCP binding and nine research guides as skills. It is generated from the Azimuth Analysis source repository; edits land there and are synced here.

If the connection fails, reply to whoever sent you this link with the error text, the app you used (Claude web, Desktop, Claude Code or ChatGPT) and your plan type. Do not send passwords or API keys.

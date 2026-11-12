# Toolbox POD MCP server

**[toolboxpod.com](https://toolboxpod.com)** · [Setup guide](https://toolboxpod.com/mcp) · [Docs](https://toolboxpod.com/docs/mcp) · [Support](https://toolboxpod.com/support)

<img src="logo.png" alt="Toolbox POD" width="96" align="right">

Toolbox POD prints custom t-shirts and hoodies to order in our own shop in Utah and ships them across the US, with no
minimum. This hosted MCP server lets your AI app work in your Toolbox POD account: design a shirt, show it on mockups,
price and order it, follow the order, and publish designs to your WooCommerce store.

This repository holds the connection details and directory listing files. The server itself is hosted by Toolbox POD:
there is nothing to install or run.

| | |
| --- | --- |
| Server URL | `https://mcp.toolboxpod.com/mcp` |
| Transport | Streamable HTTP |
| Auth | OAuth 2.1: you sign in to Toolbox POD and click **Allow**. No API key. |
| Official MCP Registry | [`com.toolboxpod/mcp`](https://registry.modelcontextprotocol.io/v0.1/servers?search=com.toolboxpod/mcp) |

## Connect

### Claude

1. In Claude, open **Customize**, then **Connectors**, click **+**, then **Add custom connector**.
2. Name it **Toolbox POD**, paste `https://mcp.toolboxpod.com/mcp` and click **Continue**.
3. A Toolbox POD page opens. Sign in and click **Allow**.

### ChatGPT

1. On chatgpt.com, open **Plugins**, click **+**, then **Add custom MCP server**.
2. Name it **Toolbox POD** and paste the server URL. Authentication: **OAuth**. Leave the client fields empty.
3. Click **Continue**, then **Create**. Sign in to Toolbox POD and click **Allow**.
4. In a chat, type **@** and pick Toolbox POD.

### Claude Code

```sh
claude mcp add --transport http --scope user toolbox-pod https://mcp.toolboxpod.com/mcp
```

Then type `/mcp` in Claude Code, pick **toolbox-pod**, then **Authenticate**. Sign in and click **Allow**.

Or install it as a Claude Code plugin (this repository is its marketplace):

```
/plugin install toolbox-pod --marketplace Toolbox-POD/toolbox-pod-mcp
```

Then type `/mcp`, pick **plugin:toolbox-pod:toolbox-pod**, then **Authenticate**.

### Codex

```sh
codex mcp add toolbox-pod --url https://mcp.toolboxpod.com/mcp
codex mcp login toolbox-pod
```

### Cursor

```json
{"mcpServers":{"toolbox-pod":{"url":"https://mcp.toolboxpod.com/mcp"}}}
```

Cursor Settings → **MCP** → **Add**, paste the entry, then click **Connect** beside toolbox-pod, sign in and click
**Allow**. The [setup guide](https://toolboxpod.com/mcp) has a one-click **Add to Cursor** button.

### Gemini CLI

```sh
gemini extensions install https://github.com/Toolbox-POD/toolbox-pod-mcp
```

Then run `/mcp auth toolbox-pod` in Gemini CLI, sign in and click **Allow**. (New: tell us if a step differs.)

### Kiro

[![Add to Kiro](https://kiro.dev/images/add-to-kiro.svg)](https://kiro.dev/launch/mcp/add?name=toolbox-pod&config=%7B%22url%22%3A%22https%3A%2F%2Fmcp.toolboxpod.com%2Fmcp%22%2C%22disabled%22%3Afalse%2C%22autoApprove%22%3A%5B%5D%7D)

Click **Add to Kiro** and approve the configuration. When Kiro shows the authenticate popup, click it, sign in to
Toolbox POD and click **Allow**.

### Any other MCP app

Add a remote server (Streamable HTTP) with `https://mcp.toolboxpod.com/mcp`. Pick OAuth if it asks; the app finds the
sign-in pages by itself.

**Check it works:** ask "Who am I on Toolbox POD?" If it names your account, you're connected.

## What you can ask it to do

- **Design.** Describe a design, share a reference image, or both, and Toolbox AI draws it, print ready. Art you
  already have works too: upload a PNG or a link to one.
- **Mockups.** See a design on a shirt in any color, on a lay-flat, folded or model photo.
- **Order.** Get today's prices, a quick estimate, then a draft order with its exact total, and follow it to tracking.
- **WooCommerce.** With a store connected: publish a design (you see a preview first), update it, or take it off.
- **Shopify.** Invite-only, coming soon.
- **Help.** Open a support request about an order and check on it.

Same prices as the website. No fee to connect and no plan needed to order. The full tool list is in the
[docs](https://toolboxpod.com/docs/mcp#tools).

## Safety

- Your AI works as you, with your role, and never more than you could do on the website.
- **Nothing is paid by default.** Until the account Owner sets a spending limit, your AI prepares orders and you pay
  for them yourself. In ChatGPT and Claude on the web it always sends you a link to pay on toolboxpod.com.
- Tools that change or spend something are marked, so your AI app asks you before it runs them.
- The Claude Code, Cursor and Grok Build plugins add a [skill](skills/toolbox-pod/SKILL.md): your AI shows the items
  and the total and waits for your yes before it orders, pays, publishes to your store or draws a design.
- Disconnect any time on the [Connections page](https://toolboxpod.com/app/connections).

## Links

[Privacy policy](https://toolboxpod.com/policies/privacy) · [Terms of service](https://toolboxpod.com/policies/terms) ·
support@toolboxpod.com · Made by Toolbox Brands LLC, Utah.

The files in this repository are MIT licensed.

[![MCP Badge](https://lobehub.com/badge/mcp/toolbox-pod-toolbox-pod-mcp)](https://lobehub.com/mcp/toolbox-pod-toolbox-pod-mcp)

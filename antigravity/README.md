# Toolbox POD

Toolbox POD prints custom t-shirts and hoodies to order in our own shop in Utah and ships them across the US, with no
minimum. This plugin connects Antigravity to Toolbox POD's hosted MCP server (`https://mcp.toolboxpod.com/mcp`,
Streamable HTTP), so your agent can work in your Toolbox POD account. There is nothing to install or run.

## Sign in

The server uses OAuth 2.1. No API key and no client ID: Antigravity finds the sign-in pages by itself.

1. Add the plugin. When its MCP server connects, Antigravity opens a Toolbox POD page in your browser. Or start it
   yourself: in the app, open **Customizations**, then **Installed**, and click **Authenticate** next to the Toolbox POD
   server; in the CLI, open `/plugin`, expand **toolbox-pod** under **Installed** and choose **Sign in**.
2. Sign in to Toolbox POD, or create an account on that page, and click **Allow**.
3. If Antigravity asks for an authorization code, copy it from the browser, paste it in and click **Submit**.

**Check it works:** ask "Who am I on Toolbox POD?" If it names your account, you're connected.

## What you can ask it to do

- **Design.** Describe a design, share a reference image, or both, and Toolbox AI draws it, print ready. Art you
  already have works too: upload a PNG or a link to one. Saved designs can be reused.
- **Mockups.** See a design on a shirt in any color, on a lay-flat, folded or model photo.
- **Order.** Get today's prices, a quick estimate, then a draft order with its exact total, and follow it to tracking.
- **WooCommerce.** With a store connected: publish a design (you see a preview first), update it, or take it off.
- **Help.** Open a support request about an order and check on it.

Same prices as the website. No fee to connect and no plan needed to order. The full tool list is in the
[docs](https://toolboxpod.com/docs/mcp#tools).

## Safety

- Your AI works as you, with your role, and never more than you could do on the website.
- **Nothing is paid by default.** Until the account Owner sets a spending limit, your AI prepares orders and you pay
  for them yourself on toolboxpod.com.
- Tools that change or spend something are marked, so Antigravity asks you before it runs them.
- The plugin adds a skill: your AI shows the items and the total and waits for your yes before it orders, pays,
  publishes to your store or draws a design.
- Disconnect any time on the [Connections page](https://toolboxpod.com/app/connections).

## Links

[Setup guide](https://toolboxpod.com/mcp) · [Docs](https://toolboxpod.com/docs/mcp) ·
[Support](https://toolboxpod.com/support) · [Privacy policy](https://toolboxpod.com/policies/privacy) ·
[Terms of service](https://toolboxpod.com/policies/terms) · support@toolboxpod.com · Made by Toolbox Brands LLC, Utah.

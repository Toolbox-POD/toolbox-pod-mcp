# Installing the Toolbox POD MCP server

Toolbox POD is a hosted remote MCP server. Do not clone, build or run anything: add the URL to the MCP client's
settings.

- URL: `https://mcp.toolboxpod.com/mcp`
- Transport: Streamable HTTP
- Auth: OAuth 2.1 with discovery (RFC 9728 protected-resource metadata, dynamic client registration). There is no API
  key and no environment variable.

Example entry for a client that reads an `mcpServers` JSON file:

```json
{
  "mcpServers": {
    "toolbox-pod": {
      "type": "streamableHttp",
      "url": "https://mcp.toolboxpod.com/mcp"
    }
  }
}
```

After adding it, the client opens a Toolbox POD sign-in page in the browser. The person signs in (or signs up) and
clicks **Allow**. Then call the `whoami` tool: it returns the person's account, role and stores.

Cline: the sign-in does not open by itself. After adding the server, run `cline mcp`, choose Authorize OAuth, then
`toolbox-pod` (in the Cline extension, click Authenticate on the server). Its tools appear only after that. The CLI's
config file is `~/.cline/data/settings/cline_mcp_settings.json`; one-line add:
`cline mcp add toolbox-pod --transport http https://mcp.toolboxpod.com/mcp`.

Docs: https://toolboxpod.com/docs/mcp

<p align="center">
  <a href="https://statsmcp.dev"><img src="https://statsmcp.dev/icon-192.png" width="96" height="96" alt="StatsMCP logo"></a>
</p>

<h1 align="center">StatsMCP</h1>

<p align="center"><strong>Official national statistics for every AI assistant.</strong></p>

<p align="center"><a href="https://statsmcp.dev">statsmcp.dev</a></p>

StatsMCP gives Claude, ChatGPT, Cursor and other AI assistants read-only access to the databases of national statistics offices, through the [Model Context Protocol](https://modelcontextprotocol.io). Every answer cites the official source and links to the table.

## Connect

Add the endpoint as a remote MCP server. It uses Streamable HTTP and needs no account or API key.

| Country  | Database        | Endpoint                      | Status  |
| -------- | --------------- | ----------------------------- | ------- |
| Slovenia | SiStat (SURS)   | `https://statsmcp.dev/si/mcp` | Live    |
| Norway   | Statbank (SSB)  | `https://statsmcp.dev/no/mcp` | Planned |
| Iceland  | Statistics Iceland | `https://statsmcp.dev/is/mcp` | Planned |

```sh
claude mcp add --transport http statsmcp-si https://statsmcp.dev/si/mcp
```

For Claude, ChatGPT, Cursor and VS Code, the steps are on [statsmcp.dev](https://statsmcp.dev).

## Principles

- **Read-only.** The servers only read public data.
- **Cited.** Each result names the statistics office and links to the table.
- **Private.** The hosted endpoint writes no logs.
- **Open.** The code is under the MIT licence.

StatsMCP is independent. It is not affiliated with or endorsed by any statistics office.

<p align="center">
  <a href="https://statsmcp.dev"><img src="https://statsmcp.dev/icon-192.png" width="96" height="96" alt="StatsMCP logo"></a>
</p>

<h1 align="center">StatsMCP</h1>

<p align="center"><strong>Official national statistics for every AI assistant.</strong></p>

<p align="center"><a href="https://statsmcp.dev">statsmcp.dev</a> · <a href="https://github.com/Stats-MCP/statsmcp">Source code</a> · <a href="https://www.npmjs.com/org/statsmcp">npm</a></p>

StatsMCP gives Claude, ChatGPT, Cursor, VS Code and other AI assistants read-only access to the databases of national statistics offices and Eurostat, through the [Model Context Protocol](https://modelcontextprotocol.io). The assistant searches more than 44,000 official tables. Every answer cites the official source and links to the table.

## Connect

Add one endpoint as a remote MCP server. It uses Streamable HTTP and needs no account or API key.

```sh
claude mcp add --transport http statsmcp https://statsmcp.dev/mcp
```

`https://statsmcp.dev/mcp` covers every office below. To connect to only one office, use `https://statsmcp.dev/<code>/mcp`:

| Code | Office |
| ---- | ------ |
| `si` | Statistical Office of the Republic of Slovenia |
| `no` | Statistics Norway |
| `ee` | Statistics Estonia |
| `fo` | Statistics Faroe Islands |
| `fi` | Statistics Finland |
| `se` | Statistics Sweden |
| `dk` | Statistics Denmark |
| `nl` | Statistics Netherlands |
| `is` | Statistics Iceland |
| `hr` | Croatian Bureau of Statistics |
| `ie` | Central Statistics Office (Ireland) |
| `ca` | Statistics Canada |
| `au` | Australian Bureau of Statistics |
| `eu` | Eurostat |

For Claude, ChatGPT, Cursor and VS Code, the steps are on [statsmcp.dev](https://statsmcp.dev). To run a server on your computer, use `npx -y @statsmcp/<office>`; the [README](https://github.com/Stats-MCP/statsmcp#databases) lists the packages.

## Principles

- **Read-only.** The servers only read public data.
- **Cited.** Each result names the statistics office and links to the table.
- **Private.** The hosted endpoint writes no logs.
- **Open.** The code is under the MIT licence. Contributions and new offices are welcome: see [CONTRIBUTING](https://github.com/Stats-MCP/statsmcp/blob/main/CONTRIBUTING.md).

StatsMCP is independent. It is not affiliated with or endorsed by any statistics office.

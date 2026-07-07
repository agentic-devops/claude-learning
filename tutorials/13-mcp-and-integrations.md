# MCP and Integrations -- Connecting Claude to External Tools

> **What you will learn:** What the Model Context Protocol (MCP) is, how it extends Claude's capabilities, and how to set up your first integration.
> **Prerequisites:** [Getting Started](03-getting-started.md)
> **Time:** 15 minutes

## What Is MCP?

The **Model Context Protocol (MCP)** is an open standard that lets Claude connect to external tools and data sources. Without MCP, Claude can only work with text you paste into the conversation. With MCP, Claude can:

- **Read files** from your computer
- **Query databases** directly
- **Interact with APIs** (GitHub, Slack, Jira, and more)
- **Search the web** for current information
- **Run code** and see the output

Think of MCP as giving Claude hands -- instead of just talking about your files, it can actually open and read them.

## How MCP Works

MCP uses a client-server architecture:

1. **MCP servers** are small programs that expose specific capabilities (reading files, querying a database, etc.)
2. **Claude** (the client) connects to these servers and can use their capabilities during conversations
3. **You control** which servers are active and what permissions they have

```
You ←→ Claude ←→ MCP Server ←→ External Tool/Data
                     │
                     ├── File System Server → Your local files
                     ├── GitHub Server → Repos, PRs, issues
                     ├── Database Server → SQL queries
                     └── Web Search Server → Live web results
```

## Available MCP Integrations

There is a growing ecosystem of MCP servers. Some popular ones:

| Integration | What It Does |
|-------------|-------------|
| **Filesystem** | Read and write files on your computer |
| **GitHub** | Manage repos, pull requests, issues, and code search |
| **Slack** | Read and send messages in Slack channels |
| **PostgreSQL / SQLite** | Query databases with natural language |
| **Brave Search** | Search the web for current information |
| **Puppeteer** | Control a web browser for scraping and testing |
| **Memory** | Give Claude persistent memory across conversations |

The full list of community-built MCP servers is available at the [MCP servers repository](https://github.com/modelcontextprotocol/servers).

## Setting Up Your First MCP Server

The simplest MCP server to start with is the **filesystem server**, which lets Claude read files from a directory on your computer.

### Step 1: Open the Claude Desktop app

MCP is configured through the desktop app (not the web interface).

### Step 2: Open settings

Go to **Settings** (or Preferences) and find the **MCP** or **Developer** section.

### Step 3: Add a server configuration

The configuration is a JSON file. Add the filesystem server:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/Users/yourname/Documents"
      ]
    }
  }
}
```

Replace `/Users/yourname/Documents` with the path to the directory you want Claude to access.

### Step 4: Restart Claude

Close and reopen the Claude Desktop app. You should see the MCP server listed as connected.

### Step 5: Test it

Start a new conversation and ask:
```text
List the files in my Documents folder.
```

Claude will use the filesystem MCP server to read your directory and respond with the actual file listing.

## Security Considerations

MCP servers have access to real systems, so treat permissions carefully:

- **Only grant access to directories you intend** -- do not point the filesystem server at your entire home directory
- **Review what each server can do** -- some servers can read AND write; understand the difference
- **Be cautious with API keys** -- servers that connect to external services need credentials; store them securely
- **You approve each action** -- Claude will ask permission before using MCP tools in a conversation

## MCP with Claude Code

If you use Claude Code (the CLI tool), MCP servers can also be configured there. Claude Code can then use these integrations while working on your codebase:

```bash
# Claude Code can use MCP servers configured in your project
# or globally in ~/.claude/settings.json
claude
> Search our GitHub repo for open issues related to authentication
> Query the staging database for users created in the last 24 hours
```

## Common Use Cases

### Connecting to your codebase
```text
# With filesystem MCP active:
Read my project's README and suggest improvements based on the
actual code structure.
```

### Working with databases
```text
# With a database MCP server:
Show me the 10 most recent orders with their status. Then identify
any orders that have been "pending" for more than 48 hours.
```

### Integrating with team tools
```text
# With GitHub MCP:
List all open pull requests in our main repo. For each one, summarize
what it changes and flag any that have been open for more than a week.
```

### Try It Yourself

**Exercise 1: Set up the filesystem server**

Follow the setup steps above to connect the filesystem MCP server to the Claude Desktop app. Point it at a directory with some documents or code. Then ask Claude to read and summarize a file.

**Exercise 2: Explore available servers**

Visit the [MCP servers repository](https://github.com/modelcontextprotocol/servers) and browse the available integrations. Identify 2-3 that would be useful for your workflow.

## Key Takeaways

- MCP is an open protocol that connects Claude to external tools and data sources
- MCP servers are small programs that expose specific capabilities (file access, database queries, API calls)
- The filesystem server is the easiest starting point -- it lets Claude read files on your computer
- MCP is configured through the Claude Desktop app or Claude Code settings
- Always review permissions and be intentional about what access you grant
- A growing ecosystem of community-built servers covers GitHub, Slack, databases, web search, and more

## Next Steps

Learn how to use Claude programmatically in [Claude API Basics](14-claude-api-basics.md).

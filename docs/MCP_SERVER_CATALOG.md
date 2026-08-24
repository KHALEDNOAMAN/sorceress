# MCP Server Catalog & Comparison

## What is MCP?
Model Context Protocol (MCP) lets AI assistants interact with external tools, APIs, and data sources through a standardized protocol.

## Popular MCP Servers

### Data & Search
| Server | Description | Language |
|--------|-------------|----------|
| web-search | Search the web via Brave/Google | Python |
| database | Query SQL/NoSQL databases | TypeScript |
| memory | Persistent knowledge graph | Python |
| filesystem | Read/write local files | TypeScript |

### Developer Tools
| Server | Description | Language |
|--------|-------------|----------|
| github | Manage repos, issues, PRs | TypeScript |
| git | Version control operations | Python |
| docker | Container management | Python |
| kubernetes | K8s cluster operations | Go |

### AI & ML
| Server | Description | Language |
|--------|-------------|----------|
| huggingface | Model inference | Python |
| langchain | Chain of thought tools | Python |
| embeddings | Vector similarity search | Python |

## Building Your Own MCP Server
```python
from mcp import Server, Tool

server = Server("my-server")

@server.tool("greet")
def greet(name: str) -> str:
    """Greet a user by name."""
    return f"Hello, {name}!"

server.run()
```

## Best Practices
- Keep tools focused and single-purpose
- Include clear descriptions for AI to understand usage
- Handle errors gracefully with informative messages
- Rate limit external API calls
- Cache responses when appropriate

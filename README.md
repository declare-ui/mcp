<p align="left">
    <img width="1280" height="192" alt="wordmark-color-transparent-1280x192" src="https://github.com/user-attachments/assets/d51c038f-7822-4ee4-beb8-f438894f7736" />
    <img width="1280" height="192" alt="wordmark-color-transparent-1280x192" src="https://github.com/user-attachments/assets/d51c038f-7822-4ee4-beb8-f438894f7736" />
</p>

# @declareui/mcp

MCP (Model Context Protocol) server that lets AI agents create, modify, validate, and document DeclareUI components through natural language.

---

## What it does

The DeclareUI MCP server exposes tools that allow AI agents like Claude, Cursor, Windsurf, and others to work with `.ui.yaml` components programmatically — generating valid component declarations, validating schemas, and compiling to target frameworks.

## Setup

Add to your MCP client configuration:

```json
{
  "mcpServers": {
    "declareui": {
      "command": "npx",
      "args": ["-y", "@declareui/mcp"]
    }
  }
}
```

### Claude Desktop / Claude Code

```json
// claude_desktop_config.json or .claude/settings.json
{
  "mcpServers": {
    "declareui": {
      "command": "npx",
      "args": ["-y", "@declareui/mcp"]
    }
  }
}
```

## Example

> *"Create a DataTable component with sorting, pagination, and a search filter."*

The agent generates valid `.ui.yaml`, validates it against the schema, and compiles to your target frameworks — all through conversation.

## Available tools

| Tool | Description |
|:-----|:------------|
| `create_component` | Generate a new `.ui.yaml` component from a description |
| `modify_component` | Update an existing component declaration |
| `validate_component` | Validate a component against the DeclareUI schema |
| `build_component` | Compile a component to target frameworks |
| `list_components` | List all components in the current project |

## Related packages

| Package | Description |
|:--------|:------------|
| [`@declareui/core`](https://github.com/declare-ui/core) | Parser, AST, and code generators |
| [`@declareui/cli`](https://github.com/declare-ui/cli) | CLI tool |
| [`@declareui/components`](https://github.com/declare-ui/components) | Pre-built component library |

## Contributing

See [CONTRIBUTING.md](https://github.com/declare-ui/.github/blob/main/CONTRIBUTING.md) for guidelines.

## License

MIT

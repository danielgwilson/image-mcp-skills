# Image MCP Skills

Public distribution repo for Image MCP skills and future recipes.

This repo intentionally contains only the install-safe skill artifact, not the private Image MCP application source.

## Current Contents

- `image-mcp/SKILL.md`
- `image-mcp/references/`
- `image-mcp/agents/`

The core Image MCP skill lives in `image-mcp/`.

This repo can also grow to include:

- additional Image MCP skills
- use-case recipes
- target-specific install metadata
- small public helper assets

## Recommended Workflow

For most agent workflows, install the CLI and use the bundled installer:

```bash
npm install -g @image-mcp/cli
image-mcp skill install --agent all
```

The flagship skill lives in the `image-mcp/` directory for direct repo-based installs and `skills.sh` style listings.

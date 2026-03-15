# Image MCP Skill

Public distribution repo for the Image MCP skill.

This repo intentionally contains only the install-safe skill artifact, not the private Image MCP application source.

## Contents

- `image-mcp/SKILL.md`
- `image-mcp/references/`
- `image-mcp/agents/`

## Recommended Workflow

For most agent workflows, install the CLI and use the bundled installer:

```bash
npm install -g @image-mcp/cli
image-mcp skill install --agent all
```

The skill itself lives in the `image-mcp/` directory for direct repo-based installs and `skills.sh` style listings.

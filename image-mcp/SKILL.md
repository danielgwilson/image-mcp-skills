---
name: image-mcp
description: Use when the user explicitly wants to generate, edit, upload, or inspect images with Image MCP via the image-mcp CLI. Also use when the user asks about Image MCP model capabilities, generation history, or Image MCP-specific image workflows.
---

# Image MCP

Use the `image-mcp` CLI for Image MCP workflows.

## Use this skill when

- the user wants to create an image with Image MCP
- the user wants to edit or remix an image with Image MCP
- the user wants to upload a local image for later editing
- the user wants to inspect Image MCP generation history
- the user wants to inspect Image MCP model capabilities

## Do not use this skill when

- the user only wants generic image analysis
- the user wants a different image provider specifically
- the task is not actually about Image MCP

## Workflow

1. Run `image-mcp doctor` or `image-mcp whoami` if auth state is unclear.
2. If auth is missing or stale, run `image-mcp login` and then `image-mcp whoami`.
3. Use `image-mcp models --json` when you need current model capability info.
4. Prefer `--json` when another agent step will consume the result.
5. Use `image-mcp create "<prompt>"` for generation tasks. It waits by default; use `--async` when you want a job id immediately.
6. Use `image-mcp edit <image-ref> "<prompt>"` for edits. Local file paths are uploaded automatically before the edit job is created.
7. Use `image-mcp job list` to recover long or interrupted runs and `image-mcp job get <job-id>` to inspect a specific job.
8. Use `image-mcp job wait <job-id> --json` when you need explicit polling instead of the default wait behavior.
9. Use `image-mcp job cancel <job-id>` when a queued or running job should be stopped.

## References

- For command usage patterns, see [references/cli-usage.md](references/cli-usage.md)
- For model selection guidance, see [references/model-selection.md](references/model-selection.md)
- For troubleshooting, see [references/troubleshooting.md](references/troubleshooting.md)

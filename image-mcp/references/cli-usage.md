# CLI Usage

Use `--json` when another tool or agent step needs structured output.

Commands below assume `image-mcp` is already on `PATH`.

If it is not installed globally yet, use:

- `npx --yes @image-mcp/cli whoami`
- `npx --yes @image-mcp/cli create "<prompt>"`
- `npx --yes @image-mcp/cli edit <image-ref> "<prompt>"`

Current commands:

- `image-mcp login`
- `image-mcp whoami`
- `image-mcp models`
- `image-mcp create "<prompt>"`
- `image-mcp edit <image-ref> "<prompt>"`
- `image-mcp upload <file-or-url>`
- `image-mcp activity`
- `image-mcp job get <job-id>`
- `image-mcp job list`
- `image-mcp job cancel <job-id>`
- `image-mcp job wait <job-id>`
- `image-mcp doctor`
- `image-mcp logout`
- `image-mcp skill install`

Useful behavior notes:

- `create` and `edit` wait for completion by default
- use `--async` on `create` or `edit` to return immediately with a job id
- `edit` accepts an Image MCP image id, remote URL, or local file path
- local file paths passed to `edit` are uploaded automatically before job creation
- use `job list` to recover from long or interrupted runs
- use `job cancel` to stop queued or in-progress jobs
- use `--poll-seconds` and `--timeout-seconds` with `job wait` for long-running jobs

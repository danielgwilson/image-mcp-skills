# Troubleshooting

If `image-mcp` is not found:

1. Install it globally with `npm install -g @image-mcp/cli`
2. Or run commands with `npx --yes @image-mcp/cli ...`

If auth fails:

1. Run `image-mcp doctor`
2. Run `image-mcp login`
3. Run `image-mcp whoami`
4. Check whether `IMAGE_MCP_API_KEY` is set and overriding local auth
5. Check the local auth file under `~/.config/image-mcp/auth.json`

If `npx` fails with npm cache permission errors:

1. Retry with a temp cache:
   `NPM_CONFIG_CACHE="$(mktemp -d)" npx --yes @image-mcp/cli whoami`
2. If that works, fix ownership under `~/.npm` later so one-off runs do not fail

If model lookup fails:

1. Verify the Image MCP base URL
2. Retry `image-mcp models --json`
3. Confirm the backend is reachable

If a job runs for a long time:

1. Re-run with `--async` to get a job id immediately
2. Use `image-mcp job wait <job-id> --json`
3. Increase `--timeout-seconds` for long 2K or 4K renders

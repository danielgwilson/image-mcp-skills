# Model Selection

Use `image-mcp models --json` for the current supported model list.

When choosing a model:

- prefer defaults unless the user asks for a specific provider or model
- check whether `resolution`, `aspect_ratio`, or `image_size` is supported before assuming a parameter exists
- use `image-mcp models --json` instead of guessing model support from memory
- ask before using unusually expensive settings when intent is ambiguous

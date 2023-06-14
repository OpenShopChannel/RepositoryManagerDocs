---
description: Treatments group for internet communication.
---

# Web

## Available Treatments

These are the treatments currently provided by the "Web" treatment group:

<table><thead><tr><th width="245">Treatment</th><th width="223">Arguments</th><th>Description</th></tr></thead><tbody><tr><td>web.download</td><td>["url", "path"]</td><td>Downloads a path from given url to a given path (creates it if doesn't exist), optionally uses user-agent specified in "source" section. Paths relative to application root.</td></tr></tbody></table>

### Example:

```json
{
    ...
    "treatments": [
        {
            "treatment": "web.download",
            "arguments": ["https://example.com/app.dol", "apps/newozero/boot.dol"]
        },
    ],
    ...
}
```

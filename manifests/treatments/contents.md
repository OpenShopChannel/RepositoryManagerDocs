---
description: Treatments group for manipulating files and directories.
---

# Contents

## Available Treatments

These are the treatments currently provided by the "Contents" treatment group:

<table><thead><tr><th width="176">Treatment</th><th width="223">Arguments</th><th>Description</th></tr></thead><tbody><tr><td>contents.move</td><td>["source", "destination"]</td><td>Moves a <mark style="color:red;"><strong>single</strong></mark> directory/file from "source" to "destination". Paths relative to application root. The "source" can contain a <a href="../../pattern-matching.md">pattern</a>.<br><br>Similar to usage of the mv command in Linux.</td></tr><tr><td>contents.delete</td><td>["path"]</td><td>Deletes a directory/file. Path relative to application root.</td></tr></tbody></table>

### Example:

```json
{
    ...
    "treatments": [
        {
            "treatment": "contents.move", "arguments": ["newozero/", "apps/newozero/"]
        },
    ],
    ...
}
```

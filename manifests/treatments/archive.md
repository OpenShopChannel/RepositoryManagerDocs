---
description: Treatments group for dealing with archives files.
---

# Archive

## Available Treatments

These are the treatments currently provided by the "Archive" treatment group:

<table><thead><tr><th width="245">Treatment</th><th width="223">Arguments</th><th>Description</th></tr></thead><tbody><tr><td>archive.extract</td><td>["path", "to_path"]</td><td>Extracts an archive at given "path" to the "to_path".</td></tr></tbody></table>

<mark style="color:red;">The archive format must be supported by Repository Manager, and have the correct file extension for the format.</mark>

For list of supported archive formats:

{% content-ref url="../../supported-archive-formats.md" %}
[supported-archive-formats.md](../../supported-archive-formats.md)
{% endcontent-ref %}

### Example:

```json
{
    ...
    "treatments": [
        {
            "treatment": "archive.extract",
            "arguments": ["default-images.zip", "apps/wiigallery/images/"]
        },
    ],
    ...
}
```

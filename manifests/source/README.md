---
description: How should the server obtain this app?
---

# Source



<figure><img src="../../.gitbook/assets/expensive-delivery.svg" alt=""><figcaption><p>Woah! Big Package!</p></figcaption></figure>

## Available Types

There is currently only one supported type.

<table><thead><tr><th width="212">Type</th><th width="165">JSON Value</th><th>Contains</th></tr></thead><tbody><tr><td>URL</td><td>"url"</td><td>Obtain application from a direct link.</td></tr><tr><td>GitHub Release</td><td>"github_release"</td><td>Obtain application from a GitHub release.</td></tr><tr><td>Manual</td><td>"manual"</td><td>Obtains nothing, leaves the job for treatments like "web.download".</td></tr></tbody></table>

### Example:

```json
{
    ...
    "source": {
        ...
        "type": "url",
        ...
    },
    ...
}
```

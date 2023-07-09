---
description: How should the server obtain this app?
---

# Source



<figure><img src="../../.gitbook/assets/expensive-delivery.svg" alt=""><figcaption><p>Woah! Big Package!</p></figcaption></figure>

## Available Types

These are the currently supported source types.

<table><thead><tr><th width="212">Type</th><th width="213">JSON Value</th><th>Contains</th></tr></thead><tbody><tr><td><a href="url/">URL</a></td><td>"url"</td><td>Obtain application from a direct link.</td></tr><tr><td><a href="github-release/">GitHub Release</a></td><td>"github_release"</td><td>Obtain application from a GitHub release.</td></tr><tr><td><a href="sourceforge-release.md">SourceForge Release</a></td><td>"sourceforge_release"</td><td>Obtain app from the SourceForge "best release".</td></tr><tr><td><a href="itchio.md">itch.io</a></td><td>"itchio"</td><td>Obtain app from itch.io.</td></tr><tr><td><a href="mediafire/">MediaFire</a></td><td>"mediafire"</td><td>Obtain app from MediaFire.</td></tr><tr><td>Manual</td><td>"manual"</td><td>Obtains nothing, leaves the job for treatments like "web.download".</td></tr></tbody></table>

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

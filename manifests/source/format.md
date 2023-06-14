---
description: '"format": "zip"'
---

# Format

{% hint style="warning" %}
**This is a required field!**
{% endhint %}

## Formats

Name of the archive format that needs to be extracted. \
<mark style="color:red;">The archive format must be supported by Repository Manager, and be correctly named according to the</mark> [<mark style="color:red;">Supported Archive Formats</mark>](../../supported-archive-formats.md) <mark style="color:red;">list.</mark>\
\
For a full list of supported formats and their names:

{% content-ref url="../../supported-archive-formats.md" %}
[supported-archive-formats.md](../../supported-archive-formats.md)
{% endcontent-ref %}

### Example:

{% code overflow="wrap" %}
```json
{
    ...
    "source": {
        ...
        "format": "zip",
        ...
    },
    ...
}
```
{% endcode %}

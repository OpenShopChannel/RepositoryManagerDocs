---
description: How should the server prepare this app for distribution?
---

# Treatments

<figure><img src="../../.gitbook/assets/repository-manager-logo.svg" alt="" width="188"><figcaption><p>Treating Apps...</p></figcaption></figure>

{% hint style="info" %}
This is very important information, that must be read before creating a manifest.
{% endhint %}

{% hint style="danger" %}
<mark style="background-color:red;">Treatments are handled in the order they are written in the manifest.</mark>



**Treatments should only be used when required.**\
e.g. for fixing a broken meta.xml, moving files to the right location, removing gamecube only files, removing duplicate files, obtaining application files, and removing unnecessary bloat.
{% endhint %}

Treatments are Repository Manager's solution for the differences in how different developers choose to distribute their apps. They are intended to ensure a consistent experience between all Open Shop Channel apps.

What exactly is that consistent experience? First, is the structure. All apps on the Open Shop Channel are distributed exactly like so:

```
root/
├─ apps/
│  ├─ slug/ (Slug of the application, as specified in the manifest)
│  │  ├─ meta.xml (Required)
│  │  ├─ icon.png (Required)
│  │  ├─ boot.dol/boot.elf (Required)
│  │  ├─ <...more application files...>
```

When writing a manifest for an app obtained from a certain place, we must ensure that it ends up in this structure, with all of the required files. Treatments are the way we do that.

Here is an example treatment, which is used for preparing NewoZero for distribution:

```json
{
    ...
    "treatments": [
        ...
        {
            "treatment": "contents.move", "arguments": ["newozero/", "apps/newozero/"]
        },
        ...
    ],
    ...
}
```

Currently, in this early stage in development, these are the available treatment groups:

{% content-ref url="contents.md" %}
[contents.md](contents.md)
{% endcontent-ref %}

{% content-ref url="meta.md" %}
[meta.md](meta.md)
{% endcontent-ref %}

{% content-ref url="web.md" %}
[web.md](web.md)
{% endcontent-ref %}

{% content-ref url="archive.md" %}
[archive.md](archive.md)
{% endcontent-ref %}

---
description: Treatments group for manipulating the meta.xml file.
---

# Meta

## Available Treatments

These are the treatments currently provided by the "Meta" treatment group:

<table><thead><tr><th width="245">Treatment</th><th width="223">Arguments</th><th>Description</th></tr></thead><tbody><tr><td>meta.remove_declaration</td><td></td><td>Removes the unicode declaration / first line of the meta.xml file. Used for fixing some broken meta.xmls.</td></tr><tr><td>meta.remove_comments</td><td></td><td>Removes comments. Helpful for when comments contain double-hyphens, which breaks xml parsing and violates the xml specification.</td></tr><tr><td>meta.set</td><td>["key", "value"]</td><td>Sets a key in the meta.xml to the given value. Can be used to override things like app name, author name and description.</td></tr><tr><td>meta.init</td><td></td><td>Solely intended for when a meta.xml is not provided by the author.<br><mark style="color:red;">Should not be used in place of "fixing" a broken file using other treatments.</mark><br><br>Creates a new meta.xml file, and pre-populates it with:<br>- "name" as specified in the <a href="../essential-information/">information</a> section.<br>- "coder" as specified in the <a href="../essential-information/">information</a> section.<br>- "version" as specified in the <a href="../essential-information/">information</a> section.<br>- "short_description": "No description provided."</td></tr></tbody></table>

### Example:

```json
{
    ...
    "treatments": [
        {
            "treatment": "meta.set", "arguments": ["name", "Newo Zero"]
        },
    ],
    ...
}
```

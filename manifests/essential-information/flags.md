---
description: '"flags": ["writes_to_nand"]'
---

# Flags

Flags is an optional dictionary that should contain within it potentially important information about an application, e.g. if it writes to nand.

Currently, these are the supported flags:



<table><thead><tr><th width="193.33333333333331">Flag</th><th>Description</th><th></th></tr></thead><tbody><tr><td>"writes_to_nand"</td><td>For applications that potentially write to NAND.</td><td>For homebrew browser specifically, adds a "[CAUTION! Writes to NAND!]" prefix to long descriptions.</td></tr><tr><td>"deprecated"</td><td>Signals this application is not recommended to use unless necessary, and an alternative should be used instead.</td><td>"This homebrew application is deprecated and should only be used when a better alternative is not available."</td></tr></tbody></table>

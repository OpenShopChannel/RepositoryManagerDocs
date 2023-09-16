---
description: '"flags": ["writes_to_nand"]'
---

# Flags

Flags is an optional dictionary that should contain within it potentially important information about an application, e.g. if it writes to nand.

Currently, these are the supported flags:



| Flag               | Description                                      |                                                                                                      |
| ------------------ | ------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| "writes\_to\_nand" | For applications that potentially write to NAND. | For homebrew browser specifically, adds a "\[CAUTION! Writes to NAND!]" prefix to long descriptions. |

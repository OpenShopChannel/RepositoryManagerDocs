---
description: '"peripherals": ["Wii Remote", "Wii Remote", "GameCube Controller"]'
---

# Peripherals

{% hint style="warning" %}
**This is a required field!**
{% endhint %}

## Peripherals

These are the peripheral types currently supported by Open Shop Channel.

<table><thead><tr><th width="160">Peripheral</th><th width="224">JSON Value</th><th></th></tr></thead><tbody><tr><td>Wii Remote</td><td>"Wii Remote"</td><td>Up to four can be included in the list. Example: ["Wii Remote", "Wii Remote", "GameCube Controller"] means the app supports up to two Wii Remotes and a GameCube Controller.</td></tr><tr><td>GameCube Controller</td><td>"GameCube Controller"</td><td></td></tr><tr><td>Nunchuk</td><td>"Nunchuk"</td><td></td></tr><tr><td>Classic Controller</td><td>"Classic Controller"</td><td></td></tr><tr><td>SDHC Support</td><td>"SDHC"</td><td>This is not really a peripheral, but it indicates support for SDHC cards to the Homebrew Browser.</td></tr><tr><td>USB Keyboard</td><td>"USB Keyboard"</td><td>USB Keyboards are supported. Not displayed on Homebrew Browser.</td></tr><tr><td>Wii Zapper</td><td>"Wii Zapper"</td><td>Wii Zapper is supported. Not displayed on Homebrew Browser.</td></tr></tbody></table>

### Example:

{% code overflow="wrap" %}
```json
{
    ...
    "information": {
        ...
        "peripherals": ["Wii Remote", "Nunchuk", "Classic Controller", "GameCube Controller", "SDHC"],
        ...
    },
    ...
}
```
{% endcode %}

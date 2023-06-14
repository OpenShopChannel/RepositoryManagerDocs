# Example manifest

To help you get a sense of how "application manifests" look like, here is one of them:

### Obtain application from URL:

{% code title="newozero.oscmeta" overflow="wrap" lineNumbers="true" %}
```json
{
    "information": {
        "name": "Newo Zero",
        "author": "Owen",
        "author_preferred_contacts": "",
        "category": "games",
        "peripherals": ["Wii Remote", "Nunchuk", "Classic Controller", "GameCube Controller", "SDHC"],
        "version": "auto"
    },
    "source": {
        "type": "url",
        "format": "zip",
        "location": "https://owensoft.net/project/newogame/dl/newozero.zip"
    },
    "treatments": [
        {
            "treatment": "contents.move",
            "arguments": ["newozero/", "apps/newozero/"]
        }
    ]
}
```
{% endcode %}

### Obtain application from GitHub releases:

{% code title="mgba.oscmeta" overflow="wrap" lineNumbers="true" %}
```json
{
    "information": {
        "name": "mGBA",
        "author": "Vicki Pfau (endrift)",
        "author_preferred_contacts": "",
        "category": "emulators",
        "peripherals": ["Wii Remote"],
        "version": "auto"
    },
    "source": {
        "type": "github_release",
        "format": "7z",
        "repository": "mgba-emu/mgba",
        "file": "mGBA-*-wii.7z"
    },
    "treatments": [
        {
            "treatment": "contents.move",
            "arguments": ["mGBA-*-wii/", "apps/mgba/"]
        }
    ]
}
```
{% endcode %}

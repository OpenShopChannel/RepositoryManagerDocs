# Retrieving Contents



<figure><img src="../.gitbook/assets/danbomovers2.png" alt="" width="375"><figcaption><p>Danbo's on the way with the apps!</p></figcaption></figure>

This endpoint returns all available applications. Specifically, successfully indexed applications.

## Get Repository Contents

<mark style="color:blue;">`GET`</mark> `/contents`

Returns all apps available in the repository.

{% tabs %}
{% tab title="200: OK Success!" %}

{% endtab %}
{% endtabs %}

Example response:

```json
[
    {
        "slug": "danbo",
        "name": "Danbo",
        "author": "Danbo",
        "authors": [],
        "category": "demos",
        "contributors": [],
        "description": {
            "short": "Danbo",
            "long": "Danbo"
        },
        "assets": {
            "icon": {
                "url": "https://hbb1.oscwii.org/api/contents/danbo/icon.png",
                "size": 16732
            },
            "archive": {
                "url": "https://hbb1.oscwii.org/api/contents/danbo/danbo.zip",
                "hash": "8df6ccfcb2f7228c0ecf45c7d579ed80",
                "size": 1337156
            },
            "binary": {
                "url": "https://hbb1.oscwii.org/unzipped_apps/danbo/apps/danbo/boot.dol",
                "hash": "b3aefb8a05100ec861448708095f3902",
                "size": 1966848
            },
            "meta": {
                "url": "https://hbb1.oscwii.org/unzipped_apps/danbo/apps/danbo/meta.xml"
            }
        },
        "flags": [],
        "package_type": "dol",
        "peripherals": [
            "wii_remote"
        ],
        "release_date": 1605484800,
        "shop": {
            "contents_size": 2733520,
            "title_id": "000100014E41D674",
            "inodes": 3,
            "title_version": 1,
            "tmd_size": 2420
        },
        "subdirectories": [],
        "supported_platforms": [
            "wii",
            "vwii",
            "wii_mini"
        ],
        "uncompressed_size": 1983880,
        "version": "v1.0"
    },
  ...
]
```

At the root level, this response contains a list of app objects. [Here is a definition for an app object](retrieving-contents.md#application-object) as returned by the API in this endpoint.

## Get Featured App:

<mark style="color:blue;">`GET`</mark> `/featured-app`

Returns the app selected by the repository to be featured, called "App of the Day" in the official Open Shop Channel website. Read here to learn how featured apps are picked.

{% tabs %}
{% tab title="200: OK Success!" %}

{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

Example response:

```json
{
    "slug": "smw-wiigii",
    "name": "Super Mario War Wii",
    "author": "Tantric",
    "authors": [],
    "category": "games",
    "contributors": [],
    "description": {
        "short": "Port of Super Mario War",
        "long": "Port of Super Mario War"
    },
    "assets": {
        "icon": {
            "url": "https://hbb1.oscwii.org/api/contents/smw-wiigii/icon.png",
            "size": 9907
        },
        "archive": {
            "url": "https://hbb1.oscwii.org/api/contents/smw-wiigii/smw-wiigii.zip",
            "hash": "865713b70d1f28a8c93dc3ec7a28b542",
            "size": 14204833
        },
        "binary": {
            "url": "https://hbb1.oscwii.org/unzipped_apps/smw-wiigii/apps/smw-wiigii/boot.dol",
            "hash": "db2316f3f8959d894e1c4cf68a4f364a",
            "size": 3246464
        },
        "meta": {
            "url": "https://hbb1.oscwii.org/unzipped_apps/smw-wiigii/apps/smw-wiigii/meta.xml"
        }
    },
    "flags": [],
    "package_type": "dol",
    "peripherals": [
        "wii_remote",
        "wii_remote",
        "wii_remote",
        "wii_remote",
        "classic_controller"
    ],
    "release_date": 1281484800,
    "shop": {
        "contents_size": 15600400,
        "title_id": "000100014E1E6C1F",
        "inodes": 3,
        "title_version": 1,
        "tmd_size": 2420
    },
    "subdirectories": [],
    "supported_platforms": [
        "wii",
        "vwii",
        "wii_mini"
    ],
    "uncompressed_size": 3258256,
    "version": "1.4"
}
```

## Application object:

<table data-full-width="true"><thead><tr><th width="209">Field</th><th width="414.3333333333333">Description</th><th>Type</th></tr></thead><tbody><tr><td>slug</td><td>Application slug. Formerly known as "internal_name" or "hbbID". The application on the repository would be called &#x3C;slug>.oscmeta.</td><td>String</td></tr><tr><td>name</td><td>The display name of the application, as specified in meta.xml (fallback value: name field on manifest)</td><td>String</td></tr><tr><td>author</td><td>The main author of the application, as specified in the meta.xml (fallback value: author field on manifest). This will be displayed as the "Publisher" in the Shop Channel, as such it must be only one author.</td><td>String</td></tr><tr><td>authors</td><td>A list of other developers of the application.</td><td>List of Strings</td></tr><tr><td>category</td><td>Name of category, as specified in the application manifest. Will always be a category declared as an available category in the <a href="retrieving-information.md">information endpoint</a> and the categories.json file in repository root.</td><td>String</td></tr><tr><td>contributors</td><td>A list of contributors (not developers) of the application.</td><td>List of Strings</td></tr><tr><td>description</td><td>Description of the application, as specified in meta.xml.</td><td><a href="retrieving-contents.md#description">Description</a></td></tr><tr><td>assets</td><td>All the available assets for this application.</td><td><a href="retrieving-contents.md#assets">Assets</a></td></tr><tr><td>flags</td><td>List of flags for this application.</td><td>List of <a href="../manifests/essential-information/flags.md">Flags</a></td></tr><tr><td>package_type</td><td>One of two values: <code>dol</code> / <code>elf</code>. This indicates the binary type of the application.</td><td>String</td></tr><tr><td>peripherals</td><td>Peripherals supported by the application.</td><td>List of <a href="../manifests/essential-information/peripherals.md">Peripherals</a></td></tr><tr><td>release_date</td><td>UNIX timestamp of the application's release date as specified in meta.xml.<br>Fallback: binary creation date.</td><td>Integer</td></tr><tr><td>shop</td><td>Information used by the Shop Channel.</td><td><a href="retrieving-contents.md#shop-information">Shop Information</a></td></tr><tr><td>subdirectories</td><td>List of additional directories to be created, updated, or backed up by the client. Relative paths. Used by Homebrew Browser.</td><td>List of Strings</td></tr><tr><td>supported_platforms</td><td>List of platforms this app supports.</td><td>List of <a href="../manifests/essential-information/platforms.md">Platforms</a></td></tr><tr><td>uncompressed_size</td><td>The size of all the files of the application, uncompressed, in bytes.</td><td>Long</td></tr><tr><td>version</td><td>Version as specified in the meta.xml.</td><td>String</td></tr></tbody></table>

### Assets

Map of application assets.

<table><thead><tr><th width="144">Field</th><th width="528">Description</th></tr></thead><tbody><tr><td>archive</td><td>The zipped application, ready for distribution.</td></tr><tr><td>binary</td><td>The DOL/ELF of the application.</td></tr><tr><td>icon</td><td>The application icon, in PNG format.</td></tr><tr><td>meta</td><td>The meta.xml file of the application.</td></tr></tbody></table>

#### Asset object:

> Fields marked with '?' are optional, as they are not available for all asset types.

<table><thead><tr><th width="115">Field</th><th width="521">Description</th><th>Type</th></tr></thead><tbody><tr><td>url</td><td>The public URL of the asset.</td><td>String</td></tr><tr><td>size?</td><td>The size of the file, in bytes.</td><td>Long</td></tr><tr><td>hash?</td><td>The MD5 checksum of the file.</td><td>String</td></tr></tbody></table>

### Description

<table><thead><tr><th width="99">Field</th><th width="549">Description</th><th>Type</th></tr></thead><tbody><tr><td>short</td><td>"short_description" in the meta.xml, this should be used in areas where the long description won't fit. Short description as specified by the application author or overridden by manifest.</td><td>String</td></tr><tr><td>long</td><td>"long_description" in the meta.xml. Long description as specified by the application author or overridden by manifest.</td><td>String</td></tr></tbody></table>

### Shop Information

<table><thead><tr><th width="159">Field</th><th width="458">Description</th><th>Type</th></tr></thead><tbody><tr><td>title_id</td><td>Title ID for this application.</td><td>String</td></tr><tr><td>title_version</td><td>Title version.</td><td>Integer</td></tr><tr><td>contents_size</td><td>The size of the packaged app + Wii Menu Banner</td><td>Long</td></tr></tbody></table>


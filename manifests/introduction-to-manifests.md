# Introduction to manifests

<figure><img src="../.gitbook/assets/needs-no-description.svg" alt="" width="305"><figcaption><p>Manifest</p></figcaption></figure>

## What are application manifests?

Application manifests are instructions for the Repository Manager server, providing it with information about how to obtain applications, their information, and finally prepare them for proper distribution.

Application manifests are generally split to several main parts:

### Essential Information

This section includes information that is necessary to distribute the application, apart from information contained in the application's meta.xml, which is obtained by the server using the instructions in the "Source" section.

It also includes fields like author name and contact information, to make it easier to contact and identify the original author if needed.

{% content-ref url="essential-information/" %}
[essential-information](essential-information/)
{% endcontent-ref %}

### Source

This part contains instructions for obtaining the application files, from their original distribution locations, such as developer websites and GitHub repositories.

{% content-ref url="source/url/" %}
[url](source/url/)
{% endcontent-ref %}

### Treatments

This one is special. It contains instructions for preparing the application for distribution on the Open Shop Channel. Usually, it is used for ensuring the directory is organized into the format the Homebrew Browser expects.

{% content-ref url="source/url/" %}
[url](source/url/)
{% endcontent-ref %}

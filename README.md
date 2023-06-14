---
description: Open Shop Channel's new-gen repository system
cover: >-
  https://images.unsplash.com/photo-1587293852726-70cdb56c2866?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHxib3hlc3xlbnwwfHx8fDE2ODQ0MzI5NTl8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Repository Manager

{% hint style="info" %}
**Note:** Repository Manager is in active development, and things can change substantially!
{% endhint %}

## Overview

Repository Manager repositories are structured in a very simple way. The repository root contains a "repository.json" file describing the repository, and a "contents" directory containing manifests for its contents. That's all.

Repository Manager repositories are not designed to be server-less, but managed by a server we call "Repository Manager", which takes the role of serving the official API, obtaining and preparing application files for distribution, and providing support for the Homebrew Browser.

<figure><img src=".gitbook/assets/danbomovers2.png" alt=""><figcaption><p>Repository Manager</p></figcaption></figure>

---
layout: default
title: SpyAgntX
nav_order: 2
has_children: false
permalink: /docs/signature/spyagntx
nav_exclude: true
---

# SpyAgntX

## High-level Description

* Year: 2017
* File Hash (SHA-256): 63e8ef385b20f68d19a38c0678d85bdcf50db70bb13f300512ba3322499df935
* Blog: https://nakedsecurity.sophos.com/2017/07/27/dont-want-your-smss-stolen-dont-download-these-android-apps/

This malware sample aims to download a payload which performs information stealing. The malware sample retrieves an executable after waiting a certain period of time and retrieving commands from the C&C server. It then aims to steal SMS messages from the user.

## Signature
---

The image of the signature can be downloaded [here](../../img/signatures/SpyAgntX.png) for closer inspection.

![](../../img/signatures/SpyAgntX.png)
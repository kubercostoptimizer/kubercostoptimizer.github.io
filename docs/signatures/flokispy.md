---
layout: default
title: FlokiSpy
nav_order: 2
has_children: false
permalink: /docs/signature/flokispy
nav_exclude: true
---

# FlokiSpy

## High-level Description

* Year: 2018
* File Hash (SHA-256): b168e64a02c3aed52b0c6f77a380420dd2495c3440c85a3b7ed99b8ac871d46a
* Blog: https://blog.trendmicro.com/trendlabs-security-intelligence/fake-banking-app-found-on-google-play-used-in-smishing-scheme/

This malware application aims to steal device and user-specific information. On launch of the application, the malware sample hides its icon, collects device information, and dynamically registers a receiver on SMS received system-wide events. Once the user receives an SMS, the sample creates two threads to (1) leak device information to the malware developer's server, and (2) leak SMS and device information to the malware developer's server. In addition, the main thread collects the device phone number and SMS message. It then leaks the information to a hardcoded number via text.

## Signature
---

The image of the signature can be downloaded [here](../../img/signatures/FlokiSpy.png) for closer inspection.

![](../../img/signatures/FlokiSpy.png)
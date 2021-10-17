---
layout: default
title: GuerillaA
nav_order: 2
has_children: false
permalink: /docs/signature/guerillaa
nav_exclude: true
---

# GuerillaA

## High-level Description

* Year: 2018
* File Hash (SHA-256): f0ea929501a599b214025f0e2d3e6d2304cc23be10f6c61c02c4ba5f05a9f0ae
* Blog: https://nakedsecurity.sophos.com/2018/05/10/watch-out-photo-editor-apps-hiding-malware-on-google-play/

This malware sample aims to perform ad-click fraud. It listens to a variety of package events (Package Added, Package Removed, Package Replaced), boot events (Boot Complete), device status (User Present), and battery events (Power Connected). The malware sample schedules a task to steal device information and retrieve ad configuration to perform ad-click fraud.

## Signature
---

The image of the signature can be downloaded [here](../../img/signatures/GuerillaA.png) for closer inspection.

![](../../img/signatures/GuerillaA.png)
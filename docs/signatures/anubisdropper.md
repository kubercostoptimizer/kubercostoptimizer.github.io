---
layout: default
title: AnubisDropper
nav_order: 2
has_children: false
permalink: /docs/signature/anubisdropper
nav_exclude: true
---

# AnubisDropper

## High-level Description

* Year: 2019
* File Hash (SHA-256): f847b80ab00228a2642c66373ad6c5053955c71796685400f2e07e99709421d5 
* Blog: https://blog.trendmicro.com/trendlabs-security-intelligence/google-play-apps-drop-anubis-banking-malware-use-motion-based-evasion-tactics/

This malware sample aims to steal information from the user. The malware sample schedules a task on a variety of network events (Wifi State Change, Connectivity Change), package events (External Applications Available, Package Removed, Package Added), device status (Screen On, Dreaming Stopped, User Present), and boot events (Boot Complete, Quickboot Poweron). It then checks to ensure the device is a user based on sandbox detection and data retrieved from motion sensors. The malware sample downloads an executable, the user installs the executable, and the executable aims to steal SMS messages (an observed behavior).

## Signature
---

The image of the signature can be downloaded [here](../../img/signatures/AnubisDropper.png) for closer inspection.

![](../../img/signatures/AnubisDropper.png)
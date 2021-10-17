---
layout: default
title: Implementation
nav_order: 1
has_children: false
permalink: /docs/Implementation
---

# Malware Collection
---

## Overview

We detail the malware collection, in a step-by-step manner, used to retrieve malware which bypasses Google Play malware. These steps include:

1. [Collecting blogs from security companies](#blog-collection)
2. [Identifying Google Play malware blogs](#identifying-google-play-malware-blogs)
3. [Malware collection and analysis](#malware-collection-and-analysis)

A detailed list of statistics is found within the following [excel sheet](../../../assets/data/excelsheets/MalwareCollectionStatistics.xlsx). 

---

## Blog Collection

Blogs were collected based on security reports. The following sections detail the collection steps.

### Identifying Security 

The resulting companies containing blog sites are described below:

1. Blackberry Cylance
2. Checkpoint
3. Comodo
4. Cybereason
5. ESET
6. FireEye
7. Fortinet
8. F-Secure
9. Kaspersky
10. MalwareBytes
11. Mcafee
12. Microsoft
13. PaloAltoNetworks
14. PandaSecurity
15. SentinelOne
16. Sophos
17. Symantec
18. TrendMicro
19. Vmware CarbonBlack

### Automated Blog Crawler

The source code of our blog crawler is available on [GitHub](https://github.com/hello-from-anon-researcher/BlogScrapeUtilities/).

---

## Identifying Google Play Malware Blogs

### Blog Categorization

We categorized the blogs into five categories, including:

1. Google Play Malware - Blogs that describe malware bypassing Google Play Store
2. Non-Google Play Malware - Blogs describing Android malware from alternative markets
3. Non-Android Malware - Blogs describing malware from systems other than Android (ex., iOS, PC, etc.)
4. Different Language - Blogs that are not in English
5. Technology/News/Promotions - Blogs which describe current technologies, trends, or product promotions

The table below lists our categorization results for all 3,455 blogs we analyzed:

|Category|2016|2017|2018|2019|2020|2021|Total|
|:-------------------------------|:------------------:|:------:|:------:|:------:|:------:|:------:|:------:|
|Google Play Malware|56|96|51|48|26|40|317|
|Non-Google Play Malware|93|76|67|44|50|23|353|
|Non-Android Malware|212|284|238|237|221|112|1,304|
|Different Language|10|24|17|21|122|71|265|
|News/Promotions|660|798|742|778|748|412|4,138|
|All|1,031|1,278|1,115|1,128|1,167|658|6,377|

A detailed list of blogs is found within the "All Blogs" sheet of the [excel sheet](../../../assets/data/excelsheets/MalwareCollectionStatistics.xlsx).

### Blog Categorization Disagreements

We summarize the distribution of disagreements by year below:

|Category|2016|2017|2018|2019|2020|2021|Total|
|:-------------------------------|:------------------:|:------:|:------:|:------:|:------:|:------:|:------:|
|Disagreements|17|19|3|10|11|8|68|

---

## Malware Collection and Analysis

### Identifying and Collecting Families

We identified duplicate families based on blogs which either: (1) contain the same indicators (file hash, package name, app name and author) or (2) refer to another blog within our list. Below is a distribution of duplicate families found per year:

|Category|2016|2017|2018|2019|2020|2021|Total|
|:-------------------------------|:------------------:|:------:|:------:|:------:|:------:|:------:|:------:|
|Ident. Families|27|59|41|34|18|7|186|
|Dup. Families|3|12|8|5|3|21|52|
|Found Families|20|47|28|21|15|5|136|
|Found Samples|89|636|301|166|37|11|1,240|

A detailed list of families found for associated blogs is found within the "Families Described and Found" sheet of the [excel sheet](../../../assets/data/excelsheets/MalwareCollectionStatistics.xlsx).

### Analyzing Google Play malware

The overall distribution of analyzed samples per year is shown below:

|Category|2016|2017|2018|2019|2020|2021|Total|
|:-------------------------------|:------------------:|:------:|:------:|:------:|:------:|:------:|:------:|
|Packer|2|2|0|3|0|1|8|
|Reflection|0|4|0|1|0|0|5|
|Cannot Find Malicious Behavior|2|2|0|0|0|0|4|
|Obfuscation|3|4|0|0|2|0|9|
|Samples Analyzed|13|35|27|17|13|4|109|

The details of analyzed malware samples is found within the "Families Described and Found" and "Samples Unable To Analyze" sheet of the [excel sheet](../../../assets/data/excelsheets/MalwareCollectionStatistics.xlsx).

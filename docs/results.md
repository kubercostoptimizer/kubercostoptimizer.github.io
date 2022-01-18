---
layout: default
title: Results
nav_order: 4
has_children: false
permalink: /docs/results
---

# Results
---
    
## Overview

Diagrams below exemplify executions of each of the compared approaches for the SockShop application. 
Rectangular boxes at the top of each diagram represent service combinations. Circles represent VM types, which are sorted by their cost. 
The color of each circle describe the execution state:

1. Green circle:  executed experiments where VM type meets the performance target.
2. Red circle: executed experiments where VM type does not meet the performance target. 
3. Orange circles: VM types that are determined not to meat the performance target because of Condition 1.
4. White circles:  are not executed VM types.


## SF :

[![](../SF.png)](../SF.png)

## SF<sub>1</sub> :
[![](../SF1.png)](../SF1.png)

## SF<sub>2</sub> :

[![](../SF2.png)](../SF2.png)

## SF<sub>3</sub> :

[![](../SF3.png)](../SF3.png)

## P :

[![](../P.png)](../P.png)

## Kuber :

[![](../Kuber.png)](../Kuber.png)


Detailed results for each of the subject applications, which correspond to Figure 4 in the paper, can be found in the attached spreadsheets
1. [Hotel Reservation Search Cost](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/Hotel_Reservation_search_cost.xlsx)
2. [Media Microsvc Search Cost](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/Media_Microsvc_search_cost.xlsx)
3. [Social Network Search Cost](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/Social_Network_search_cost.xlsx)
4. [Sockshop Search Cost](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/sockshop_search_cost.xlsx)
5. [Hotel Reservation Execution Time](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/Hotel_Reservation_exe_time.xlsx)
6. [Media Microsvc Execution TIme](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/Media_microsvc_exe_time.xlsx)
7. [Social Network Execution Time](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/Social_network_exe_time.xlsx)
8. [Sockshop Execution Time](https://github.com/kubercostoptimizer/kubercostoptimizer.github.io/raw/main/sockshop_exe_time.xlsx)

---

Table 5.1 shows time spent by each of the approaches, separately in each of
the phases (setting up VMs for the experiments, executing the experiments, and
running the WIP algorithm) and in total. While KUBER take 53 hours on average
(the last column), the other three approaches execute for hundreds hours on an
average. In fact, the total execution time of all the experiments is more than four months.

| App               | SortFind |        |     |       | SortFind + Condition 1 |        |     |       | SortFind + Condition 2 |        |     |       | SortFind + Condition 3 |        |     |       | Kuber |        |     |       |
|-------------------|:--------:|--------|-----|-------|:----------------------:|--------|-----|-------|:----------------------:|--------|-----|-------|:----------------------:|--------|-----|-------|:-----:|--------|-----|-------|
|                   | Setup    | Exper. | WID | Total | Setup                  | Exper. | WID | Total | Setup                  | Exper. | WID | Total | Setup                  | Exper. | WID | Total | Setup | Exper. | WID | Total |
| Hotel Reservation | >395     | >158   | 0   | >553  | 55                     | 22     | 0   | 77    | 150                    | 60     | 16  | 226   | 55                     | 22     | 2   | 79    | 15    | 6      | 7   | 28    |
| Media Service     | >372     | >149   | 0   | >521  | 150                    | 60     | 0   | 210   | 412                    | 165    | 36  | 613   | 90                     | 36     | 2   | 128   | 30    | 12     | 15  | 57    |
| Social Network    | >362     | >145   | 0   | >507  | 245                    | 98     | 0   | 343   | 322                    | 129    | 26  | 477   | 357                    | 143    | 5   | 505   | 58    | 23     | 22  | 103   |
| Sock Shop         | >265     | >106   | 0   | >371  | 20                     | 8      | 0   | 28    | 130                    | 52     | 7   | 189   | 60                     | 24     | 1   | 85    | 10    | 4      | 12  | 26    |
| Average           | >348     | >139   | 0   | >487  | 117                    | 47     | 0   | 164   | 253                    | 101    | 21  | 375   | 140                    | 56     | 2.5 | 198   | 28    | 11     | 14  | 53    |




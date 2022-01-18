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

Table below shows time spent by each of the approaches, separately in each of
the phases (setting up VMs for the experiments, executing the experiments, and
running the WIP algorithm) and in total. While KUBER take 53 hours on average
(the last column), the other three approaches execute for hundreds hours on an
average. In fact, the total execution time of all the experiments is more than four months.

<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">App</th>
    <th class="tg-c3ow" colspan="4">SortFind</th>
    <th class="tg-c3ow" colspan="4">SortFind + Condition 1</th>
    <th class="tg-c3ow" colspan="4">SortFind + Condition 2</th>
    <th class="tg-c3ow" colspan="4">SortFind + Condition 3</th>
    <th class="tg-c3ow" colspan="4">Kuber</th>
  </tr>
  <tr>
    <th class="tg-c3ow">Setup</th>
    <th class="tg-c3ow">Exper.</th>
    <th class="tg-c3ow">WID</th>
    <th class="tg-c3ow">Total</th>
    <th class="tg-c3ow">Setup</th>
    <th class="tg-c3ow">Exper.</th>
    <th class="tg-c3ow">WID</th>
    <th class="tg-c3ow">Total</th>
    <th class="tg-c3ow">Setup</th>
    <th class="tg-c3ow">Exper.</th>
    <th class="tg-c3ow">WID</th>
    <th class="tg-c3ow">Total</th>
    <th class="tg-c3ow">Setup</th>
    <th class="tg-c3ow">Exper.</th>
    <th class="tg-c3ow">WID</th>
    <th class="tg-c3ow">Total</th>
    <th class="tg-c3ow">Setup</th>
    <th class="tg-c3ow">Exper.</th>
    <th class="tg-c3ow">WID</th>
    <th class="tg-c3ow">Total</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">Hotel Reservation</td>
    <td class="tg-c3ow">&gt;395</td>
    <td class="tg-c3ow">&gt;158</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">&gt;553</td>
    <td class="tg-c3ow">55</td>
    <td class="tg-c3ow">22</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">77</td>
    <td class="tg-c3ow">150</td>
    <td class="tg-c3ow">60</td>
    <td class="tg-c3ow">16</td>
    <td class="tg-c3ow">226</td>
    <td class="tg-c3ow">55</td>
    <td class="tg-c3ow">22</td>
    <td class="tg-c3ow">2</td>
    <td class="tg-c3ow">79</td>
    <td class="tg-c3ow">15</td>
    <td class="tg-c3ow">6</td>
    <td class="tg-c3ow">7</td>
    <td class="tg-c3ow">28</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Media Service</td>
    <td class="tg-c3ow">&gt;372</td>
    <td class="tg-c3ow">&gt;149</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">&gt;521</td>
    <td class="tg-c3ow">150</td>
    <td class="tg-c3ow">60</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">210</td>
    <td class="tg-c3ow">412</td>
    <td class="tg-c3ow">165</td>
    <td class="tg-c3ow">36</td>
    <td class="tg-c3ow">613</td>
    <td class="tg-c3ow">90</td>
    <td class="tg-c3ow">36</td>
    <td class="tg-c3ow">2</td>
    <td class="tg-c3ow">128</td>
    <td class="tg-c3ow">30</td>
    <td class="tg-c3ow">12</td>
    <td class="tg-c3ow">15</td>
    <td class="tg-c3ow">57</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Social Network</td>
    <td class="tg-c3ow">&gt;362</td>
    <td class="tg-c3ow">&gt;145</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">&gt;507</td>
    <td class="tg-c3ow">245</td>
    <td class="tg-c3ow">98</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">343</td>
    <td class="tg-c3ow">322</td>
    <td class="tg-c3ow">129</td>
    <td class="tg-c3ow">26</td>
    <td class="tg-c3ow">477</td>
    <td class="tg-c3ow">357</td>
    <td class="tg-c3ow">143</td>
    <td class="tg-c3ow">5</td>
    <td class="tg-c3ow">505</td>
    <td class="tg-c3ow">58</td>
    <td class="tg-c3ow">23</td>
    <td class="tg-c3ow">22</td>
    <td class="tg-c3ow">103</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Sock Shop</td>
    <td class="tg-c3ow">&gt;265</td>
    <td class="tg-c3ow">&gt;106</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">&gt;371</td>
    <td class="tg-c3ow">20</td>
    <td class="tg-c3ow">8</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">28</td>
    <td class="tg-c3ow">130</td>
    <td class="tg-c3ow">52</td>
    <td class="tg-c3ow">7</td>
    <td class="tg-c3ow">189</td>
    <td class="tg-c3ow">60</td>
    <td class="tg-c3ow">24</td>
    <td class="tg-c3ow">1</td>
    <td class="tg-c3ow">85</td>
    <td class="tg-c3ow">10</td>
    <td class="tg-c3ow">4</td>
    <td class="tg-c3ow">12</td>
    <td class="tg-c3ow">26</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Average</td>
    <td class="tg-c3ow">&gt;348</td>
    <td class="tg-c3ow">&gt;139</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">&gt;487</td>
    <td class="tg-c3ow">117</td>
    <td class="tg-c3ow">47</td>
    <td class="tg-c3ow">0</td>
    <td class="tg-c3ow">164</td>
    <td class="tg-c3ow">253</td>
    <td class="tg-c3ow">101</td>
    <td class="tg-c3ow">21</td>
    <td class="tg-c3ow">375</td>
    <td class="tg-c3ow">140</td>
    <td class="tg-c3ow">56</td>
    <td class="tg-c3ow">2.5</td>
    <td class="tg-c3ow">198</td>
    <td class="tg-c3ow">28</td>
    <td class="tg-c3ow">11</td>
    <td class="tg-c3ow">14</td>
    <td class="tg-c3ow">53</td>
  </tr>
</tbody>
</table>

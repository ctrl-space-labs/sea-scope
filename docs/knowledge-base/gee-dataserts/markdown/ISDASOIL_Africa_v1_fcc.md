



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

iSDAsoil Fertility Capability Classification


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
==============================================================================================================================================








Dataset Availability
2001\-01\-01T00:00:00Z–2017\-01\-01T00:00:00Z
Dataset Provider


[iSDA](https://isda-africa.com/)



Earth Engine Snippet


`ee.Image("ISDASOIL/Africa/v1/fcc")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_fcc)





Tags


[africa](/earth-engine/datasets/tags/africa)
[isda](/earth-engine/datasets/tags/isda)
[soil](/earth-engine/datasets/tags/soil)
fcc








#### Description



Soil fertility capability classification derived using slope, chemical,
and physical soil properties. For more information about this layer, please
visit [this page](https://www.isda-africa.com/isdasoil/faq/#faq7).


The classes for the 'fcc' band apply to pixel values that must be
back\-transformed with `x modulo 3000`.


In areas of dense jungle (generally over central Africa), model accuracy is
low and therefore artifacts such as banding (striping) might be seen.


Soil property predictions were made by
[Innovative Solutions for Decision Agriculture Ltd. (iSDA)](https://isda-africa.com/)
at 30 m pixel size using machine learning coupled with remote sensing data
and a training set of over 100,000 analyzed soil samples.


Further information can be found in the
[FAQ](https://www.isda-africa.com/isdasoil/faq/) and
[technical information documentation](https://www.isda-africa.com/isdasoil/technical-information/). To submit an issue or request support, please visit
[the iSDAsoil site](https://isda-africa.com/isdasoil).





### Bands



**Pixel Size**
  
30 meters



**Bands**




| Name | Min | Max | Description |
| --- | --- | --- | --- |
| `fcc` | 0 | 1853 | Fertility Capability Classification. Styling has been made according to the number of fertility constraints:* 0 constraints: \#1a9641 * 1 constraint: \#fff1af * 2 constraints: \#feb66a * 3 constraints: \#f3854e * 4 constraints: \#e54f35 * 5 or more constraints: \#d7191c |


**fcc Class Table**




| Value | Color | Description |
| --- | --- | --- |
| 0 | \#1a9641 | No constraints |
| 2 | \#fff1af | Gravel |
| 4 | \#fff1af | Slope |
| 6 | \#feb66a | Gravel, Slope |
| 8 | \#fff1af | High erosion risk: textual contrast |
| 10 | \#feb66a | Gravel, High erosion risk: textual contrast |
| 12 | \#feb66a | Slope, High erosion risk: textual contrast |
| 14 | \#f3854e | Gravel, Slope, High erosion risk: textual contrast |
| 17 | \#feb66a | Shallow, High erosion risk: shallow depth |
| 19 | \#f3854e | Shallow, Gravel, High erosion risk: shallow depth |
| 21 | \#f3854e | Shallow, Slope, High erosion risk: shallow depth |
| 23 | \#e54f35 | Shallow, Gravel, Slope, High erosion risk: shallow depth |
| 25 | \#f3854e | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth |
| 27 | \#e54f35 | Shallow, Gravel, High erosion risk: textual contrast, High erosion risk: shallow depth |
| 29 | \#e54f35 | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth |
| 31 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth |
| 36 | \#feb66a | Slope, High erosion risk: steep slope |
| 38 | \#f3854e | Gravel, Slope, High erosion risk: steep slope |
| 44 | \#f3854e | Slope, High erosion risk: textual contrast, High erosion risk: steep slope |
| 46 | \#e54f35 | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope |
| 53 | \#e54f35 | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope |
| 55 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope |
| 61 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope |
| 63 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope |
| 128 | \#fff1af | Al Toxicity |
| 130 | \#feb66a | Gravel, Al Toxicity |
| 132 | \#feb66a | Slope, Al Toxicity |
| 134 | \#f3854e | Gravel, Slope, Al Toxicity |
| 136 | \#feb66a | High erosion risk: textual contrast, Al Toxicity |
| 140 | \#f3854e | Slope, High erosion risk: textual contrast, Al Toxicity |
| 164 | \#f3854e | Slope, High erosion risk: steep slope, Al Toxicity |
| 166 | \#e54f35 | Gravel, Slope, High erosion risk: steep slope, Al Toxicity |
| 172 | \#e54f35 | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Al Toxicity |
| 256 | \#fff1af | Calcareous |
| 258 | \#feb66a | Gravel, Calcareous |
| 260 | \#feb66a | Slope, Calcareous |
| 262 | \#f3854e | Gravel, Slope, Calcareous |
| 264 | \#feb66a | High erosion risk: textual contrast, Calcareous |
| 266 | \#f3854e | Gravel, High erosion risk: textual contrast, Calcareous |
| 268 | \#f3854e | Slope, High erosion risk: textual contrast, Calcareous |
| 270 | \#e54f35 | Gravel, Slope, High erosion risk: textual contrast, Calcareous |
| 273 | \#f3854e | Shallow, High erosion risk: shallow depth, Calcareous |
| 275 | \#e54f35 | Shallow, Gravel, High erosion risk: shallow depth, Calcareous |
| 277 | \#e54f35 | Shallow, Slope, High erosion risk: shallow depth, Calcareous |
| 279 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, Calcareous |
| 281 | \#e54f35 | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous |
| 283 | \#d7191c | Shallow, Gravel, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous |
| 285 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous |
| 287 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous |
| 292 | \#f3854e | Slope, High erosion risk: steep slope, Calcareous |
| 294 | \#e54f35 | Gravel, Slope, High erosion risk: steep slope, Calcareous |
| 300 | \#e54f35 | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous |
| 302 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous |
| 309 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous |
| 311 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous |
| 317 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous |
| 319 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous |
| 512 | \#fff1af | Low K |
| 514 | \#feb66a | Gravel, Low K |
| 516 | \#feb66a | Slope, Low K |
| 518 | \#f3854e | Gravel, Slope, Low K |
| 520 | \#feb66a | High erosion risk: textual contrast, Low K |
| 522 | \#f3854e | Gravel, High erosion risk: textual contrast, Low K |
| 524 | \#f3854e | Slope, High erosion risk: textual contrast, Low K |
| 526 | \#e54f35 | Gravel, Slope, High erosion risk: textual contrast, Low K |
| 529 | \#f3854e | Shallow, High erosion risk: shallow depth, Low K |
| 531 | \#e54f35 | Shallow, Gravel, High erosion risk: shallow depth, Low K |
| 533 | \#e54f35 | Shallow, Slope, High erosion risk: shallow depth, Low K |
| 535 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, Low K |
| 537 | \#e54f35 | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K |
| 539 | \#d7191c | Shallow, Gravel, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K |
| 541 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K |
| 543 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K |
| 548 | \#f3854e | Slope, High erosion risk: steep slope, Low K |
| 550 | \#e54f35 | Gravel, Slope, High erosion risk: steep slope, Low K |
| 556 | \#e54f35 | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Low K |
| 558 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Low K |
| 565 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Low K |
| 567 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Low K |
| 573 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Low K |
| 575 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Low K |
| 640 | \#feb66a | Al Toxicity, Low K |
| 642 | \#f3854e | Gravel, Al Toxicity, Low K |
| 644 | \#f3854e | Slope, Al Toxicity, Low K |
| 646 | \#e54f35 | Gravel, Slope, Al Toxicity, Low K |
| 648 | \#f3854e | High erosion risk: textual contrast, Al Toxicity, Low K |
| 650 | \#e54f35 | Gravel, High erosion risk: textual contrast, Al Toxicity, Low K |
| 652 | \#e54f35 | Slope, High erosion risk: textual contrast, Al Toxicity, Low K |
| 676 | \#e54f35 | Slope, High erosion risk: steep slope, Al Toxicity, Low K |
| 678 | \#d7191c | Gravel, Slope, High erosion risk: steep slope, Al Toxicity, Low K |
| 684 | \#d7191c | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Al Toxicity, Low K |
| 768 | \#feb66a | Calcareous, Low K |
| 770 | \#f3854e | Gravel, Calcareous, Low K |
| 772 | \#f3854e | Slope, Calcareous, Low K |
| 774 | \#e54f35 | Gravel, Slope, Calcareous, Low K |
| 776 | \#f3854e | High erosion risk: textual contrast, Calcareous, Low K |
| 778 | \#e54f35 | Gravel, High erosion risk: textual contrast, Calcareous, Low K |
| 780 | \#e54f35 | Slope, High erosion risk: textual contrast, Calcareous, Low K |
| 782 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, Calcareous, Low K |
| 785 | \#e54f35 | Shallow, High erosion risk: shallow depth, Calcareous, Low K |
| 787 | \#d7191c | Shallow, Gravel, High erosion risk: shallow depth, Calcareous, Low K |
| 789 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, Calcareous, Low K |
| 791 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, Calcareous, Low K |
| 793 | \#d7191c | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, Low K |
| 795 | \#d7191c | Shallow, Gravel, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, Low K |
| 797 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, Low K |
| 799 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, Low K |
| 804 | \#e54f35 | Slope, High erosion risk: steep slope, Calcareous, Low K |
| 806 | \#d7191c | Gravel, Slope, High erosion risk: steep slope, Calcareous, Low K |
| 812 | \#d7191c | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous, Low K |
| 814 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous, Low K |
| 821 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K |
| 823 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K |
| 829 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K |
| 831 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K |
| 1024 | \#fff1af | High leaching potential |
| 1026 | \#feb66a | Gravel, High leaching potential |
| 1028 | \#feb66a | Slope, High leaching potential |
| 1030 | \#f3854e | Gravel, Slope, High leaching potential |
| 1032 | \#feb66a | High erosion risk: textual contrast, High leaching potential |
| 1036 | \#f3854e | Slope, High erosion risk: textual contrast, High leaching potential |
| 1041 | \#f3854e | Shallow, High erosion risk: shallow depth, High leaching potential |
| 1060 | \#f3854e | Slope, High erosion risk: steep slope, High leaching potential |
| 1152 | \#feb66a | Al Toxicity, High leaching potential |
| 1154 | \#f3854e | Gravel, Al Toxicity, High leaching potential |
| 1156 | \#f3854e | Slope, Al Toxicity, High leaching potential |
| 1160 | \#f3854e | High erosion risk: textual contrast, Al Toxicity, High leaching potential |
| 1164 | \#e54f35 | Slope, High erosion risk: textual contrast, Al Toxicity, High leaching potential |
| 1188 | \#e54f35 | Slope, High erosion risk: steep slope, Al Toxicity, High leaching potential |
| 1280 | \#feb66a | Calcareous, High leaching potential |
| 1281 | \#f3854e | Shallow, Calcareous, High leaching potential |
| 1282 | \#f3854e | Gravel, Calcareous, High leaching potential |
| 1284 | \#f3854e | Slope, Calcareous, High leaching potential |
| 1286 | \#e54f35 | Gravel, Slope, Calcareous, High leaching potential |
| 1288 | \#f3854e | High erosion risk: textual contrast, Calcareous, High leaching potential |
| 1290 | \#e54f35 | Gravel, High erosion risk: textual contrast, Calcareous, High leaching potential |
| 1292 | \#e54f35 | Slope, High erosion risk: textual contrast, Calcareous, High leaching potential |
| 1294 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, Calcareous, High leaching potential |
| 1297 | \#e54f35 | Shallow, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1299 | \#d7191c | Shallow, Gravel, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1301 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1303 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1305 | \#d7191c | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1307 | \#d7191c | Shallow, Gravel, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1309 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, High leaching potential |
| 1316 | \#e54f35 | Slope, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1318 | \#d7191c | Gravel, Slope, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1324 | \#d7191c | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1326 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1333 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1335 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1341 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, High leaching potential |
| 1536 | \#feb66a | Low K, High leaching potential |
| 1537 | \#f3854e | Shallow, Low K, High leaching potential |
| 1538 | \#f3854e | Gravel, Low K, High leaching potential |
| 1540 | \#f3854e | Slope, Low K, High leaching potential |
| 1541 | \#e54f35 | Shallow, Slope, Low K, High leaching potential |
| 1542 | \#e54f35 | Gravel, Slope, Low K, High leaching potential |
| 1544 | \#f3854e | High erosion risk: textual contrast, Low K, High leaching potential |
| 1546 | \#e54f35 | Gravel, High erosion risk: textual contrast, Low K, High leaching potential |
| 1548 | \#e54f35 | Slope, High erosion risk: textual contrast, Low K, High leaching potential |
| 1550 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, Low K, High leaching potential |
| 1553 | \#e54f35 | Shallow, High erosion risk: shallow depth, Low K, High leaching potential |
| 1555 | \#d7191c | Shallow, Gravel, High erosion risk: shallow depth, Low K, High leaching potential |
| 1557 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, Low K, High leaching potential |
| 1559 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, Low K, High leaching potential |
| 1561 | \#d7191c | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K, High leaching potential |
| 1563 | \#d7191c | Shallow, Gravel, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K, High leaching potential |
| 1565 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K, High leaching potential |
| 1567 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Low K, High leaching potential |
| 1572 | \#e54f35 | Slope, High erosion risk: steep slope, Low K, High leaching potential |
| 1573 | \#d7191c | Shallow, Slope, High erosion risk: steep slope, Low K, High leaching potential |
| 1574 | \#d7191c | Gravel, Slope, High erosion risk: steep slope, Low K, High leaching potential |
| 1580 | \#d7191c | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Low K, High leaching potential |
| 1582 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Low K, High leaching potential |
| 1589 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Low K, High leaching potential |
| 1591 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Low K, High leaching potential |
| 1597 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Low K, High leaching potential |
| 1599 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Low K, High leaching potential |
| 1664 | \#f3854e | Al Toxicity, Low K, High leaching potential |
| 1666 | \#e54f35 | Gravel, Al Toxicity, Low K, High leaching potential |
| 1668 | \#e54f35 | Slope, Al Toxicity, Low K, High leaching potential |
| 1670 | \#d7191c | Gravel, Slope, Al Toxicity, Low K, High leaching potential |
| 1672 | \#e54f35 | High erosion risk: textual contrast, Al Toxicity, Low K, High leaching potential |
| 1674 | \#d7191c | Gravel, High erosion risk: textual contrast, Al Toxicity, Low K, High leaching potential |
| 1676 | \#d7191c | Slope, High erosion risk: textual contrast, Al Toxicity, Low K, High leaching potential |
| 1700 | \#d7191c | Slope, High erosion risk: steep slope, Al Toxicity, Low K, High leaching potential |
| 1702 | \#d7191c | Gravel, Slope, High erosion risk: steep slope, Al Toxicity, Low K, High leaching potential |
| 1708 | \#d7191c | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Al Toxicity, Low K, High leaching potential |
| 1792 | \#f3854e | Calcareous, Low K, High leaching potential |
| 1793 | \#e54f35 | Shallow, Calcareous, Low K, High leaching potential |
| 1794 | \#e54f35 | Gravel, Calcareous, Low K, High leaching potential |
| 1796 | \#e54f35 | Slope, Calcareous, Low K, High leaching potential |
| 1798 | \#d7191c | Gravel, Slope, Calcareous, Low K, High leaching potential |
| 1800 | \#e54f35 | High erosion risk: textual contrast, Calcareous, Low K, High leaching potential |
| 1802 | \#d7191c | Gravel, High erosion risk: textual contrast, Calcareous, Low K, High leaching potential |
| 1804 | \#d7191c | Slope, High erosion risk: textual contrast, Calcareous, Low K, High leaching potential |
| 1806 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, Calcareous, Low K, High leaching potential |
| 1809 | \#d7191c | Shallow, High erosion risk: shallow depth, Calcareous, Low K, High leaching potential |
| 1811 | \#d7191c | Shallow, Gravel, High erosion risk: shallow depth, Calcareous, Low K, High leaching potential |
| 1813 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, Calcareous, Low K, High leaching potential |
| 1815 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, Calcareous, Low K, High leaching potential |
| 1817 | \#d7191c | Shallow, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, Low K, High leaching potential |
| 1821 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, Calcareous, Low K, High leaching potential |
| 1828 | \#d7191c | Slope, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |
| 1830 | \#d7191c | Gravel, Slope, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |
| 1836 | \#d7191c | Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |
| 1838 | \#d7191c | Gravel, Slope, High erosion risk: textual contrast, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |
| 1845 | \#d7191c | Shallow, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |
| 1847 | \#d7191c | Shallow, Gravel, Slope, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |
| 1853 | \#d7191c | Shallow, Slope, High erosion risk: textual contrast, High erosion risk: shallow depth, High erosion risk: steep slope, Calcareous, Low K, High leaching potential |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* Hengl, T., Miller, M.A.E., Križan, J., et al. African soil properties and nutrients
mapped at 30 m spatial resolution using two\-scale ensemble machine learning.
Sci Rep 11, 6130 (2021\).
[doi:10\.1038/s41598\-021\-85639\-y](https://doi.org/10.1038/s41598-021-85639-y)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varraw=ee.Image("ISDASOIL/Africa/v1/fcc").select(0);

varconverted=ee.Image(raw.mod(3000).copyProperties(raw));

Map.setCenter(25,-3,2);

Map.addLayer(converted,{},"Fertility Capability Classification");
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/ISDASOIL/ISDASOIL_Africa_v1_fcc)


[iSDAsoil Fertility Capability Classification](/earth-engine/datasets/catalog/ISDASOIL_Africa_v1_fcc)

Soil fertility capability classification derived using slope, chemical, and physical soil properties. For more information about this layer, please visit this page. The classes for the 'fcc' band apply to pixel values that must be back\-transformed with x modulo 3000\. In areas of dense jungle (generally over central Africa), model …

 ISDASOIL/Africa/v1/fcc,
 africa,isda,soil

2001\-01\-01T00:00:00Z/2017\-01\-01T00:00:00Z



 \-35\.22 \-31\.46 37\.98 57\.08
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets









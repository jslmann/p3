---
title       : Canadian Chronic Disease Data Exploration
subtitle    : 
author      : J. Mann 
job         : aspiring data scientist
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, quiz, interactive, shiny]              # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## The Data

In this project, we choose to explore data published by the Canadian
government on chronic disease. The original data can be found here:
[Chronic Disease Data](http://www.phac-aspc.gc.ca/data-donnees/hpcdp-pspmc/assets/ccdss-scsmc-eng.csv)

An explanation of the variables can be found here: [Chronic Disease Variables](http://www.phac-aspc.gc.ca/data-donnees/hpcdp-pspmc/assets/EN_CanadianAggregateDatasets.docx)



---

## The Visualisation Choices

In this project, I initially worked with the `ggvis` library as it seemed most flexible and integrates very nicely with the `dplyr` library. However, one difficulty I encountered was that dynamic subsetting was somewhat clumsy. For this reason, I switched to the googleVis library which provides a lot of functionality “out of the box”. There may be some sacrifice in flexibility for this choice.

---  

## Results

<!-- MotionChart generated in R 3.1.1 by googleVis 0.5.5 package -->
<!-- Sun Sep 21 14:51:04 2014 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataMotionChartID8e7d3539b166 () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 "Apples",
2008,
"West",
98,
78,
20,
"2008-12-31" 
],
[
 "Apples",
2009,
"West",
111,
79,
32,
"2009-12-31" 
],
[
 "Apples",
2010,
"West",
89,
76,
13,
"2010-12-31" 
],
[
 "Oranges",
2008,
"East",
96,
81,
15,
"2008-12-31" 
],
[
 "Bananas",
2008,
"East",
85,
76,
9,
"2008-12-31" 
],
[
 "Oranges",
2009,
"East",
93,
80,
13,
"2009-12-31" 
],
[
 "Bananas",
2009,
"East",
94,
78,
16,
"2009-12-31" 
],
[
 "Oranges",
2010,
"East",
98,
91,
7,
"2010-12-31" 
],
[
 "Bananas",
2010,
"East",
81,
71,
10,
"2010-12-31" 
] 
];
data.addColumn('string','Fruit');
data.addColumn('number','Year');
data.addColumn('string','Location');
data.addColumn('number','Sales');
data.addColumn('number','Expenses');
data.addColumn('number','Profit');
data.addColumn('string','Date');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartMotionChartID8e7d3539b166() {
var data = gvisDataMotionChartID8e7d3539b166();
var options = {};
options["width"] =    600;
options["height"] =    500;

    var chart = new google.visualization.MotionChart(
    document.getElementById('MotionChartID8e7d3539b166')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "motionchart";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartMotionChartID8e7d3539b166);
})();
function displayChartMotionChartID8e7d3539b166() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartMotionChartID8e7d3539b166"></script>
 
<!-- divChart -->
  
<div id="MotionChartID8e7d3539b166" 
  style="width: 600; height: 500;">
</div>
   Disease Fiscal.Year Gender Age.Group Population Incidence Prevalence
1 Diabetes        1999      F    1 to 4     737388       204        450
2 Diabetes        1999      F    5 to 9    1031916       324       1458
3 Diabetes        1999      F  10 to 14    1019154       450       2634
4 Diabetes        1999      F  15 to 19    1029258       534       3870
5 Diabetes        1999      F  20 to 24    1021968       828       5256
6 Diabetes        1999      F  25 to 29    1066554      1434       7968
  Mortality.with.Disease Mortality.without.Disease
1                      0                       168
2                      6                       120
3                      0                       114
4                      6                       336
5                     12                       312
6                     24                       360
  Hospitalization.with.Disease..Person.Count
1                                        198
2                                        324
3                                        546
4                                        804
5                                       1032
6                                       1656
  Hospitalization.with.Disease..Separation.Count
1                                            282
2                                            456
3                                            822
4                                           1404
5                                           1812
6                                           2760
  Hospitalization.with.Disease..Days.Stay
1                                    1290
2                                    1746
3                                    3750
4                                    7512
5                                   10074
6                                   14850
  Hospitalization.without.Disease..Person.Count
1                                         27834
2                                         18924
3                                         17724
4                                         48714
5                                         91344
6                                        137232
  Hospitalization.without.Disease..Separation.Count
1                                             34962
2                                             22950
3                                             22740
4                                             63354
5                                            116526
6                                            167430
  Hospitalization.without.Disease..Days.Stay
1                                     100884
2                                      68970
3                                      95448
4                                     244218
5                                     379056
6                                     545748
  Physician.Visit.with.Disease..Person.Count
1                                        444
2                                       1416
3                                       2556
4                                       3750
5                                       5076
6                                       7704
  Physician.Visit.with.Disease..Visit.Count
1                                      5604
2                                     13278
3                                     25920
4                                     45528
5                                     68688
6                                    116808
  Physician.Visit.without.Disease..Person.Count
1                                        511098
2                                        635304
3                                        595878
4                                        659262
5                                        672462
6                                        716058
  Physician.Visit.without.Disease..Visit.Count
1                                      3192204
2                                      2818734
3                                      2504922
4                                      4077084
5                                      5209392
6                                      6319782
  General.Physician.Visit.with.Disease..Person.Count
1                                                396
2                                               1200
3                                               2136
4                                               3438
5                                               4860
6                                               7416
  General.Physician.Visit.with.Disease..Visit.Count
1                                              2430
2                                              5466
3                                             10176
4                                             23862
5                                             39858
6                                             66972
  General.Physician.Visit.without.Disease..Person.Count
1                                                470280
2                                                582114
3                                                553776
4                                                636552
5                                                657768
6                                                698580
  General.Physician.Visit.without.Disease..Visit.Count
1                                              2333076
2                                              2065518
3                                              1830624
4                                              3124248
5                                              3913344
6                                              4443474
  Specialist.Visit.with.Disease..Person.Count
1                                         408
2                                        1254
3                                        2334
4                                        3186
5                                        4026
6                                        6186
  Specialist.Visit.with.Disease..Visit.Count
1                                       3168
2                                       7800
3                                      15738
4                                      21594
5                                      28818
6                                      49824
  Specialist.Visit.without.Disease..Person.Count
1                                         236142
2                                         265020
3                                         246342
4                                         294918
5                                         341670
6                                         409848
  Specialist.Visit.without.Disease..Visit.Count
1                                        856944
2                                        751140
3                                        672852
4                                        950346
5                                       1293174
6                                       1873590

---

## Interesting Observations

Probably the most interesting observation at this point is why seemingly identical
code works for somebody else in a slidify presentation but not for me...


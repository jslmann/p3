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
<!-- Sun Sep 21 14:18:06 2014 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataMotionChartID8bfc5b7d7cb6 () {
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
function drawChartMotionChartID8bfc5b7d7cb6() {
var data = gvisDataMotionChartID8bfc5b7d7cb6();
var options = {};
options["width"] =    600;
options["height"] =    500;

    var chart = new google.visualization.MotionChart(
    document.getElementById('MotionChartID8bfc5b7d7cb6')
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
callbacks.push(drawChartMotionChartID8bfc5b7d7cb6);
})();
function displayChartMotionChartID8bfc5b7d7cb6() {
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
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartMotionChartID8bfc5b7d7cb6"></script>
 
<!-- divChart -->
  
<div id="MotionChartID8bfc5b7d7cb6" 
  style="width: 600; height: 500;">
</div>

---

## Interesting Observations

Probably the most interesting observation at this point is why seemingly identical
code works for somebody else in a slidify presentation but not for me...


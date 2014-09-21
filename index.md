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


```r
require(googleVis)
plot(gvisMotionChart(Fruits, "Fruit", "Year",
                     options=list(width=600, height=400)))
```

```
## starting httpd help server ... done
```

```r
Sys.time()
```

[1] "2014-09-21 14:05:14 MDT"

---

## Interesting Observations

Probably the most interesting observation at this point is why seemingly identical
code works for somebody else in a slidify presentation but not for me...


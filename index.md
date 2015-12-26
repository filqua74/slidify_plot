---
title       : Macroeconomics in Europe ( App )
subtitle    : Project for Coursera Data Science Specialization
author      : Filqua74
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

Primary scope of the application is to apply what I learned in the Data Product course from Coursera. The application retrieve some data from Eurostat and provide an interactive interface to web users in order to produce comparison plot about some macroeconomic variables.

Main characteristics are:

* Retrieve data from Eurostat using SDMX
* Provide user web interface for plot customization (through shiny)
* Provide comparison plot using ggplot2

The application is available at <a href="https://filqua74.shinyapps.io/EcoPlot">shinyapps</a>.


--- .class #id 

## Original data

The data used for the project is the Eurostat GDP table retrieved in SDMX. It can be downloaded from this <a href="http://ec.europa.eu/eurostat/estat-navtree-portlet-prod/BulkDownloadListing?file=data/naida_10_gdp.sdmx.zip">url</a>.

After download, data have been converted as data frame and some columns type changed. The main characteristic of the final data frame are:


```
## 'data.frame':	148277 obs. of  8 variables:
##  $ FREQ       : Factor w/ 1 level "A": 1 1 1 1 1 1 1 1 1 1 ...
##  $ unit       : Factor w/ 6 levels "CLV_I10","CLV_PCH_PRE",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ na_item    : Factor w/ 29 levels "B11","B1G","B1GQ",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ geo        : Factor w/ 183 levels "AU","BR","CA",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ TIME_FORMAT: Factor w/ 1 level "P1Y": 1 1 1 1 1 1 1 1 1 1 ...
##  $ TIME_PERIOD: chr  "1975" "1976" "1977" "1978" ...
##  $ OBS_VALUE  : chr  "-118.9" "-122.3" "-141.5" "-149.3" ...
##  $ OBS_STATUS : chr  NA NA NA NA ...
```

--- .class #id 

## Plot generation

This is an example of plot ( related to GDP ) has been produced by the R code of the application. The same R code is part of the markdown of this slide.

<img src="assets/fig/unnamed-chunk-2-1.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" style="display: block; margin: auto;" />

--- .class #id 

## Available options

It is possible to plot these variables:

* Gross domestic product at market prices
* External balance of goods and services
* Final consumption expenditure

Time period spans 1975 to 2014. Data about several European countries are available like Germany, Spain, France and so on.

This is an application for learning purpose of the author, please refer to the original data from Eurostat for professional usage.





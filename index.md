---
title       : Banting API Reading
subtitle    : From 1 August 2013 until 5 February 2015
author      : Thong Chee Wei
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

This presentation aims to introduce a Shiny application to allow exploratory data analysis of the hourly Air Pollutant Index (API) trend of a place called Banting in Selangor, Malaysia. API reading from Banting is often used as one of the benchmark to indicate the air quality in the state of Selangor.

---

## Application Description

The API data used for the application are from 1 August 2013 until 5 February 2015. This application can be used to explore the API for a particular month of a year which are selectable and the corresponding hourly trend will be displayed.

This application can be accessed at the following URL:

https://cheeweit.shinyapps.io/data_product/

---

## Screenshot of the application

<div style='text-align: center;'>
    <img height='400' src='screenshot.png' />
</div>

---

## Sample of code used for plotting




```r
ggplot(data=selected.data, aes(x=selected.data$Hour, y=selected.data$API)) +
        geom_smooth(color="red") + labs(x="Hour", y="API")
```

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png)

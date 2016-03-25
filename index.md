---
title       : Pick the car for your budget!
subtitle    : Cousera - Develop Data Product
author      : Peter Tan
job         : Car Sales Consultant
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : Darkula      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

# Every Day Problem

After riding through the gasline price roller coaster, even though we are at the down side of the price cycle, it is in everyone's fear if one day the price would shoot up again.  In order to prevent a family budget crisis, "Pick the car for your budget" is the app that will help you select the car that will not break your bank but gives you the horse power you are looking for.

--- 

# How To Use It


To use this app, you will need to define the following requirement first:

1. Total Gasline Budget you have planned for the year.
2. Total estimated mileage you need to drive for a year.
3. Average gasline price in miles per gallon format.
4. Select the cylinder options for the car you wish to drive.
5. Define the horse power range of the car you wish to drive.  After all, if the result meets your budget, you might want to pick the car that can give you the highest power output.
6. Pick your flavor: Automatic transmission or Manual transmission.

Once you have make your selection, the avaialble car choices that matches your need will be display on the body of the page.  You can sort this data set by clicking the arrows on at the column name or search by text for each column.  

After you are satisfy with your options, then it is time to make your selection of the car that matches your need.

---

# The Logic Behind the App

This app is using the mtcars dataset provided by the datasets package.

We have displayed the sample data below:


```r
library(datasets)
head(mtcars)
```

```
##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
```
GaslineSpendingPerYr = input$totalMileage/mpg*input$avgGasPrice

To compute the gasline spending per year, we take your input on expected total mileage travel per year, divided by miles per gallon for each vehicle and multiple by estimated average gasline price per gallon.

---

# Feedbacks

Thank you for your participation.  I hope this app will help you avoid hitting the family budget crisis.

You can test it out by accessing the following URL:

https://alucarrd.shinyapps.io/CouseraShiny/

The source code is stored at the following repository:

https://github.com/Alucarrd/DataProduct









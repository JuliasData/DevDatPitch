---
title       : Prediction of Diamond Value by Carat, Clarity, Cut and Color
subtitle    : Course Project Coursera Developing Data Products  
author      : JuliasData  
job         : 
framework   : io2012       # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]         # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides


--- .class #id 

## Summary

### The purpose of the shiny app is to estimate the value of a diamond, for which the so-called 4 C's are known.

---

## Method

The diamonds dataset from the ggplot2 package is used to create a linear regression model using the variables Carat, Clarity, Cut and Color as predictors for price in USD. 

In the shiny app, the values for these 4 factors needs to be entered and the predicted price will be returned.


---

## The Model
The dataset from the ggplot 2 contains the prices and other attributes of almost 54,000 diamonds. The model is a simple linear regression model:


```r
fitModel <- lm(price ~ carat + cut + clarity + color, data = diamonds)
```


It explains 91.59% of the variance, which is sufficient to allow a good prediction for new values.

---

## The Application

The following variables needs to be entered and the predicted price will be returned:

### Carat - weight of the diamond 
Numerical value from .01, to 3.

### Cut - quality of the cut
Choose from Fair, Good, Very Good, Premium, Ideal

### Colour -  diamond colour
Choose from J (worst) to D (best)

### Clarity -  a measurement of how clear the diamond is
Choose from I1 (worst), SI1, SI2, VS1, VS2, VVS1, VVS2, IF (best)




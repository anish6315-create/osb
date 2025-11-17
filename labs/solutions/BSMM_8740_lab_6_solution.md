# Lab 11 – Time Series Methods (Q11 Solutions)

## Introduction
In this lab-style exercise, we explore ARIMA forecasting methods using daily stock prices of the five major Canadian banks. The goal is to follow the same workflow demonstrated in Lab 6: exploring the data, creating time-based resampling splits, defining recipes and models, calibrating forecasts, and evaluating accuracy.  
Here, we focus specifically on forecasting the closing price of CIBC (symbol: **CM**) using an ARIMA model.

---

## Packages
```r
library(tidyverse)
library(tidymodels)
library(timetk)
library(modeltime)
The Data

The data was obtained from Yahoo Finance using the tq_get() function.
The dataset includes daily closing prices for:

TD

BMO

BNS

RBC

CM

We load the prepared CSV:

arima_data <- readr::read_csv("data/stock_data.csv", show_col_types = FALSE)

Exercise 1: EDA (Plotting the Data)

Plot the closing prices for all five banks using the timetk visualization functions.

SOLUTION:
arima_data %>%
  plot_time_series(
    .date_var   = date,
    .value      = close,
    .facet_vars = symbol,
    .interactive = FALSE,
    .title = "Daily Closing Prices for Major Canadian Banks"
  )

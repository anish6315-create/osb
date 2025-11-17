---
title: "BSMM 8740 – Q11 Solutions"
format:
  html:
    theme: cosmo
    toc: true
    toc-location: left
    smooth-scroll: true
    code-fold: true
editor: source
---

# Introduction
This page contains the complete solutions for Q11 using ARIMA forecasting on CIBC (CM) stock prices.  
The format and layout follow the same design as the Lab 6 solution page.

# Packages
```{r}
library(tidyverse)
library(tidymodels)
library(timetk)
library(modeltime)

Data
Writing

arima_data <- read_csv("data/stock_data.csv")

Exercise 1: Plot the Data
Writing

arima_data %>%
plot_time_series(
date, close,
.facet_vars = symbol
)

Exercise 2: Train / Test Split
Writing

cm_data <- arima_data %>% filter(symbol == "CM")

splits <- time_series_split(
cm_data,
initial = "10 years",
assess = "1 year"
)

splits %>%
tk_time_series_cv_plan() %>%
plot_time_series_cv_plan(date, close)

Exercise 3: Recipe, ARIMA Model, Workflow
Writing

time_rec <- recipe(close ~ ., data = training(splits))

model_spec_arima <- arima_reg() %>% set_engine("auto_arima")

workflow_fit_arima <- workflow() %>%
add_recipe(time_rec) %>%
add_model(model_spec_arima) %>%
fit(training(splits))

Exercise 4: Calibration and Forecast
Writing

models_tbl <- modeltime_table(workflow_fit_arima)

calibration_tbl <- models_tbl %>%
modeltime_calibrate(testing(splits))

calibration_tbl %>%
modeltime_forecast(
new_data = testing(splits),
actual_data = cm_data
) %>%
plot_modeltime_forecast()

Exercise 5: Accuracy Metrics
Writing

accuracy_tbl <- calibration_tbl %>% modeltime_accuracy()
accuracy_tbl


---

# ✔ Step 3 — Commit the file  
Click **Commit changes**.

---

# ✔ Step 4 — Upload your CSV file  
In your repo root, click:

**Add file → Upload file**

Upload:



data/stock_data.csv


(Make sure the path is exactly `/data/stock_data.csv`.)

---

# ✔ Step 5 — Wait 30–60 seconds
GitHub Pages will rebuild automatically.

Then go to:

👉 **https://anish6315-create.github.io/osb/labs/solutions/Q11_solutions.html**

🎉 And you will see your Q11 solutions in the **exact same design** as:

https://bsmm-8740-fall-2025.github.io/osb/labs/solutions/BSMM_8740_lab_6_solutions.html

---


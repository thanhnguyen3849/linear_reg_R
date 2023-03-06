---
title: "__Linear Regression in R Practice__"
author:
  name: "Author: Le Thanh Nguyen"
date: "`r format(Sys.time(), '%d %B %Y')`" 
output:
  bookdown::html_document2:
    number_sections: TRUE
    code_folding: hide
    df_print: kable
    toc: true
    toc_float: 
      toc_collapsed: true
    theme: spacelab
    highlight: zenburn
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

```{r "basic_packages"}
pacman::p_load(psych, xray, boot, ggplot2, texreg, DT, excelR, plotly, wrapr, 
               sjmisc, sjlabelled, sjstats, sjPlot, dplyr, forcats, knitr,
               kableExtra, captioner, tidyverse, magick, stringr, Rmisc, 
               gridExtra, bookdown, ggthemes, summarytools, randomForest, car,
               pastecs, rmarkdown)
```   

```{r "load the csv"}
copd <- read.csv("https://raw.githubusercontent.com/thanhnguyen3849/linear_reg_R/main/COPD_student_dataset.csv")
```

```{r "histogram"}
hist(copd$MWT1Best, main = "Histogram of MWT1Best ", xlab = "MWT1Best")
```


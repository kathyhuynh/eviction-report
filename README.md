---
title: "Evictions in San Francisco"
output: html_document
---

```{r setup, include=FALSE}
library(knitr)
knitr::opts_chunk$set(echo = F)
source("analysis.R")
```

# Summary

Since 2015, there have been `r num_evictions` in the city of San Francisco. Here is a table of the zip codes most heavily impacted:

```{r}
kable(by_zip, col.names = c("Zip code", "Number of Evictions"))
```

# Time trends
There have been notable spikes in evictions that warrant additional investigation:

```{r}
by_month_plot
```

## Spatial Trends
Here are the locations of evictions in 2017:

```{r, warning=FALSE}
evictions_plot
```
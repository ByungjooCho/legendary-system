---
title: "Untitled"
author: "Buil Lee"
date: "2018년 7월 22일"
output: html_document
---

```{r setup, include = FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

```{r include = FALSE}
library(leaflet)
library(dplyr)
```

```{r}
leaflet() %>% 
  setView(lng = 127.103471, lat = 37.518333, zoom = 16) %>% 
  addTiles() %>% 
  addMarkers(lng = 127.103471, lat = 37.518333, popup = "장미3차아파트")
```

# 1. 일변량 질적 자료의 분석
## 1.1 빈도표
```{r}
library(ggplot2)
table(diamonds$cut)
prop.table(table(diamonds$cut))*100
```

<br>

## 1.2 막대그래프
```{r}
barplot(table(diamonds$cut), col = "purple")
```

```{r echo=FALSE}
barplot(table(diamonds$cut), col = "purple")
```

<br>

다이아몬드의 가격의 평균은 `r mean(diamonds$price)`이다.


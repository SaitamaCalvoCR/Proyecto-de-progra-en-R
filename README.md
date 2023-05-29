# Proyecto-de-progra-en-R
a
---
title: "Index"
---

```{r}
library(readr)
library(dplyr)
library(ggplot2)
library(plotly)
library(DT)
library(quarto)
```

```{r}
coffee_data <- read.csv("C:/Users/PC/Desktop/Proyecto, tarea 2/coffee-quality.csv")
```

```{r}
datatable(coffee_data[, c("Country_of_Origin", "Variety", "Color", "Altitude", "Total_Cup_Points")])

```

```{r}
ggplotly(
  ggplot(coffee_data, aes(x = Total_Cup_Points)) +
  geom_histogram() +
  labs(title = "Distribución de Total_Cup_Points",
       x = "Total_Cup_Points",
       y = "Frecuencia") +
  geom_density(adjust = 1)
)


```

```{r}
ggplotly(
  ggplot(coffee_data, aes(x = Altitude, y = Total_Cup_Points)) +
  geom_point() +
  labs(title = "Altitude vs Total_Cup_Points",
       x = "Altitude",
       y = "Total_Cup_Points") +
  geom_smooth(method = "lm")
)

```

```{r}
ggplotly(
  ggplot(coffee_data, aes(x = Color, y = Total_Cup_Points)) +
  geom_boxplot() +
  labs(title = "Total_Cup_Points por Color",
       x = "Color",
       y = "Total_Cup_Points") +
  theme(axis.text.x = element_text(angle = 45, hjust = 1))
)

```

```{r}
theme_void(
  base_size = 11,
  base_family = "",
  base_line_size = base_size/22,
  base_rect_size = base_size/22
)
```

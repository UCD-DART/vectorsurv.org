---
title: Charts & Plot Functions
---

`vectorsurvR` includes built-in plot functions for common surveillance visualizations. For custom charts, the `ggplot2` package integrates directly with data returned by the package's retrieval and calculation functions.

---

## Built-in Plot Functions

### plotInvasiveSums()

Plots the cumulative sum (line) and interval sum (bars) of invasive mosquito species over a target year. The shape of the cumulative curve indicates the rate of activity — a convex slope means an accelerating catch rate, concave means a slowing rate, and a straight line means a constant rate.

```r
plotInvasiveSums(token, interval, target_year, invasive_species, agency_ids = NULL)
```

| Argument           | Description                                            |
| ------------------ | ------------------------------------------------------ |
| `token`            | Token from `getToken()`                                |
| `interval`         | `"CollectionDate"`, `"Week"`, `"Biweek"`, or `"Month"` |
| `target_year`      | Year to plot                                           |
| `invasive_species` | Species name(s) as a character vector                  |
| `agency_ids`       | Optional agency filter                                 |

**Example**

```r
plotInvasiveSums(
  token            = token,
  interval         = "Week",
  target_year      = 2020,
  invasive_species = "Ae aegypti"
)
```

**Output:** A combined bar and line chart. Bars show the count per interval; the line shows the running cumulative total for the year.

---

### plotVectorAbundance()

Creates a time series chart showing vector abundance across multiple years, with the target year highlighted in red. An optional historical average line provides context for identifying anomalies against baseline conditions.

> This function accepts only **one species at a time**. To compare multiple species, call the function in a loop.

```r
plotVectorAbundance(token, interval, target_year, start_year = NULL, end_year = NULL,
                    species, trap, agency_ids = NULL, sex = "female",
                    trapnight_min = 1, trapnight_max = NULL)
```

| Argument        | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| `token`         | Token from `getToken()`                                                        |
| `interval`      | `"CollectionDate"`, `"Week"`, `"Biweek"`, or `"Month"`                         |
| `target_year`   | Focal year to highlight in red                                                 |
| `start_year`    | Start of comparison range. Defaults to 5 years before `target_year`.           |
| `end_year`      | End of comparison range. Defaults to `target_year`.                            |
| `species`       | A single species name. Use `unique(data$species_display_name)` to see options. |
| `trap`          | Trap type filter. Use `unique(data$trap_acronym)` to see options.              |
| `agency_ids`    | Optional agency filter                                                         |
| `sex`           | Sex type filter. Default is `"female"`.                                        |
| `trapnight_min` | Minimum trap nights to include (default: 1)                                    |
| `trapnight_max` | Maximum trap nights to include. Defaults to maximum available.                 |

**Examples**

```r
# Single species abundance trend
plotVectorAbundance(
  token       = token,
  interval    = "Week",
  target_year = 2024,
  species     = "Cx pipiens",
  trap        = "CO2"
)

# Plot multiple species by looping
for (sp in c("Cx tarsalis", "Cx pipiens")) {
  p <- plotVectorAbundance(
    token       = token,
    interval    = "Week",
    target_year = 2024,
    species     = sp,
    trap        = "CO2",
    agency_ids  = 55
  )
  print(p)
}
```

**Output:** A line chart with one line per historical year (grey) and the target year in red. If 5 or more prior years of data are available, a dashed historical mean line is overlaid.

---

## Custom Charts with ggplot2

`ggplot2` builds charts by layering components onto a base object. It works directly with any data frame returned by the package's calculation functions.

### Species Counts by Month

```r
library(ggplot2)
library(lubridate)
library(dplyr)

# Add month column
sample_collections$month <- as.factor(month(sample_collections$collection_date))

# Summarize by month and species
collections_sums <- sample_collections %>%
  filter(species_display_name %in% c(
    "Cx tarsalis", "Cx pipiens", "An freeborni", "Ae melanimon"
  )) %>%
  group_by(month, species_display_name) %>%
  summarise(sum_count = sum(num_count, na.rm = TRUE), .groups = "drop")

# Stacked bar chart
ggplot(collections_sums, aes(x = month, y = sum_count, fill = species_display_name)) +
  geom_bar(stat = "identity") +
  labs(
    title = "Mosquito Counts by Month and Species",
    x     = "Month",
    y     = "Total Count",
    fill  = "Species"
  ) +
  theme_minimal()
```

**Output:** A stacked bar chart with one bar per month, segments colored by species.

### Species Composition Bar Chart

```r
species_summary <- sample_collections %>%
  group_by(species_display_name) %>%
  summarise(total_count = sum(num_count, na.rm = TRUE), .groups = "drop") %>%
  arrange(desc(total_count)) %>%
  mutate(pct = round(total_count / sum(total_count) * 100, 1))

ggplot(species_summary, aes(x = reorder(species_display_name, total_count),
                             y = total_count, fill = species_display_name)) +
  geom_bar(stat = "identity", show.legend = FALSE, width = 0.6) +
  geom_text(aes(label = paste0(pct, "%")), hjust = -0.2, size = 3.5) +
  coord_flip() +
  scale_y_continuous(expand = expansion(mult = c(0, 0.15))) +
  labs(title = "Species Composition", x = NULL, y = "Total Mosquitoes Collected") +
  theme_minimal()
```

**Output:** A horizontal bar chart showing each species ranked by total count, with percentage labels.

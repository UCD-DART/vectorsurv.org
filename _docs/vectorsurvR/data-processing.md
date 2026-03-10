---
title: Data Processing
---

Before running calculations, it is often helpful to explore and reshape your data. This section covers subsetting, filtering, grouping, and pivoting using base R and `dplyr`.

> **Important:** Do not subset or filter your collections or pools data before passing it into calculator functions — doing so may drop columns those functions depend on. Apply any subsetting or filtering *after* calculations are complete.

---

## Subsetting Columns

You can reduce a data frame to only the columns you need using column names or index numbers.

```r
# View all available column names
colnames(sample_collections)
#>  [1] "id"                   "collection_date"      "agency_code"
#>  [4] "site_code"            "species_display_name" "sex_type"
#>  [7] "num_count"            "trap_acronym"         "trap_nights"
#> [10] "surv_year"            ...

# Subset by column name
sample_collections[c("collection_date", "species_display_name", "num_count")]

# Subset by column index
sample_collections[c(2, 4, 10)]

# Save a subset to a new variable
collections_subset <- sample_collections[c("collection_date", "species_display_name", "num_count")]
```

---

## Filtering with dplyr

`dplyr` provides SQL-like tools for filtering and transforming data frames. The pipe operator `%>%` passes data from one step to the next.

```r
library(dplyr)

# Filter to a single species
collections_pip <- sample_collections %>%
  filter(species_display_name == "Cx pipiens")

# Filter to multiple species using %in%
collections_pip_tar <- sample_collections %>%
  filter(species_display_name %in% c("Cx pipiens", "Cx tarsalis"))

# Select specific columns only
sample_collections %>%
  select(collection_date, species_display_name, num_count) %>%
  head()
#>   collection_date species_display_name num_count
#> 1      2020-06-01          Cx pipiens        14
#> 2      2020-06-01         Cx tarsalis         3
#> 3      2020-06-03          Cx pipiens         8
```

For a deeper introduction to `dplyr`, see the [Data Carpentry guide](https://datacarpentry.org/dc_zurich/R-ecology/04-dplyr.html).

---

## Grouping and Summarising

Use `group_by()` and `summarise()` to aggregate data across any grouping variable.

```r
# Total mosquitoes counted per species per date
sample_collections %>%
  group_by(collection_date, species_display_name) %>%
  summarise(total_count = sum(num_count, na.rm = TRUE)) %>%
  head()
#>   collection_date species_display_name total_count
#> 1      2020-06-01          Cx pipiens          22
#> 2      2020-06-01         Cx tarsalis           3
#> 3      2020-06-03          Cx pipiens          16

# Average count per species per date
sample_collections %>%
  group_by(collection_date, species_display_name) %>%
  summarise(avg_count = mean(num_count, na.rm = TRUE)) %>%
  head()
```

---

## Pivoting (Long ↔ Wide Format)

API data arrives in **long format** — one row per observation. Use `tidyr` to reshape it into **wide format** (one column per species), which is useful for exports and custom tables.

```r
library(tidyr)

collections_wide <- pivot_wider(
  sample_collections,
  names_from  = c("species_display_name", "sex_type"),
  values_from = "num_count"
)
```

**Output:** Each unique combination of species and sex becomes its own column, with counts as values.

See `?pivot_wider` and `?pivot_longer` in R for additional options.

---

## Counting Unique Collection Events

A single collection event can produce multiple rows in the data — for example, one row for female mosquitoes and one for males of the same species at the same site. When counting collection events, always use `n_distinct()` on the collection ID rather than `nrow()`.

```r
# WRONG — counts rows, not unique events
nrow(collections)

# CORRECT — counts unique collection events
n_distinct(collections$id)
```

This distinction matters when reporting collection totals in summaries and reports.

---
title: Tables
---

`vectorsurvR` includes built-in table functions that format and display surveillance data. For additional styling, the `kableExtra` and `DT` packages integrate cleanly with the package output.

---

## getPoolsComparisionTable()

Produces a frequency table of positive and negative pool counts by year and species. Useful for a quick cross-tabulation of testing activity across time.

```r
getPoolsComparisionTable(pools, target_disease, separate_by = "species")
```

| Argument | Description |
|---|---|
| `pools` | Pools data from `getPools()` |
| `interval` | Time interval: `"Week"`, `"Biweek"`, or `"Month"` |
| `target_disease` | Disease acronym (e.g., `"WNV"`). Use `unique(pools$target_acronym)` to see options. |
| `separate_by` | Split table by `"species"` (default) or other grouping variables. |

**Example**

```r
getPoolsComparisionTable(
  sample_pools,
  interval       = "Week",
  target_disease = "WNV",
  separate_by    = "species"
)
#>              Species  Positive  Negative  Total
#> 1         Cx pipiens         8       142    150
#> 2        Cx tarsalis         3        97    100
```

---

## getSpeciesTable()

Generates a formatted summary table for mosquito species collection data. Calculates counts, trap events, and optionally abundance or cumulative totals over a chosen time interval. Output format adjusts automatically based on whether you are knitting to HTML, PDF, or Word.

```r
getSpeciesTable(token, target_year, interval = NULL, cumulative = FALSE,
                include_abundance = FALSE, species = NULL, trap = NULL,
                sex = "female", separate_by = NULL, output_format = "auto",
                caption = NULL, agency_id = NULL)
```

| Argument | Description |
|---|---|
| `token` | Token from `getToken()` |
| `target_year` | Year to summarize data for |
| `interval` | Time interval: `"CollectionDate"`, `"Week"`, `"Biweek"`, `"Month"`, or `NULL` for a full-year summary |
| `cumulative` | Logical. If `TRUE`, adds cumulative count and trap event columns. Default is `FALSE`. |
| `include_abundance` | Logical. If `TRUE`, adds an abundance column (non-cumulative and interval-based only). Default is `FALSE`. |
| `species` | Optional species filter. Use `unique(data$species_display_name)`. |
| `trap` | Optional trap type filter. Use `unique(data$trap_acronym)`. |
| `sex` | Sex type filter. Default is `"female"`. Use `unique(data$sex_type)` to see options. |
| `separate_by` | Optional grouping column. Accepts `"site"`, `"city"`, `"county"`, `"agency"`, `"trap"`, or `"spatial"`. |
| `output_format` | Table format: `"auto"` (default), `"html"`, `"pdf"`, or `"word"`. `"auto"` detects the knit output format automatically. |
| `caption` | Optional custom caption string. Auto-generated if not provided. |
| `agency_id` | Optional agency filter |

**Examples**

```r
# Year-level summary for two species
getSpeciesTable(
  token       = token,
  target_year = 2024,
  species     = c("Cx tarsalis", "Cx pipiens")
)
#>        Species  Count  TrapEvents
#> 1   Cx pipiens   4821         612
#> 2  Cx tarsalis   2104         612

# Monthly breakdown with abundance and county grouping
getSpeciesTable(
  token             = token,
  target_year       = 2024,
  interval          = "Month",
  include_abundance = TRUE,
  separate_by       = "county",
  species           = "Cx tarsalis"
)

# Cumulative weekly counts
getSpeciesTable(
  token       = token,
  target_year = 2024,
  interval    = "Week",
  cumulative  = TRUE,
  species     = "Ae aegypti"
)
```

> The `output_format = "auto"` setting detects whether you are knitting to HTML, PDF, or Word and applies the appropriate table styling automatically. No manual changes needed when switching between output formats.

---

## Styled Tables with kableExtra

The `kableExtra` package adds styling, row/column highlighting, merged headers, and footnotes to any data frame. It works across HTML, PDF, and Word output formats.

```r
library(kableExtra)

ab_output <- getAbundance(
  sample_collections,
  interval    = "Biweek",
  species     = c("Cx tarsalis", "Cx pipiens"),
  trap        = "CO2",
  separate_by = "species"
)

ab_output %>%
  head() %>%
  kbl(col.names = c("Agency", "Year", "Biweek", "Count", "County",
                    "Species", "Trap Events", "Trap Type", "Abundance")) %>%
  kable_styling(
    bootstrap_options = c("striped", "hover"),
    font_size         = 13,
    latex_options     = "scale_down"
  ) %>%
  footnote(
    general       = "Biweekly abundance for Cx. tarsalis and Cx. pipiens in CO2 traps.",
    general_title = ""
  )
```

You can also highlight specific rows and columns:

```r
table(sample_collections$trap_acronym, sample_collections$surv_year) %>%
  kbl(align = "c") %>%
  kable_paper(full_width = FALSE, lightable_options = "striped") %>%
  add_header_above(c("Trap Type" = 1, "Surveillance Year" = 7)) %>%
  footnote(general = "Trap deployments by year.", general_title = "") %>%
  row_spec(c(3, 6, 7), background = "#fef9e7") %>%
  column_spec(4, background = "#fdebd0")
```

For a full reference see the [kableExtra documentation](https://CRAN.R-project.org/package=kableExtra).

---

## Interactive Tables with DT

The `DT` package creates sortable, searchable, paginated tables. These are ideal for HTML reports where users need to explore large datasets. They are not compatible with PDF or Word output.

```r
library(DT)

ab_output %>%
  datatable(
    colnames = c("Agency", "Year", "Biweek", "Count", "County",
                 "Species", "Trap Events", "Trap Type", "Abundance"),
    options  = list(pageLength = 10, scrollX = TRUE)
  )
```

> Use `kableExtra` when your report needs to work across HTML, PDF, and Word. Use `DT` when your report is HTML-only and interactivity is valuable.

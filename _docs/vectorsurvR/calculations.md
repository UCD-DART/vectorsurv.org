---
title: Calculations
---

The calculation functions in `vectorsurvR` replicate the methods used in the VectorSurv Gateway calculators. All functions require collections or pools data retrieved via `getArthroCollections()` or `getPools()`.

---

## getAbundance()

Calculates mosquito abundance — the average number of mosquitoes caught per trap night — over a specified time interval.

$$\text{Abundance} = \frac{\text{Total Individuals}}{\text{Total Trap Nights}}$$

```r
getAbundance(collections, interval, agency = NULL, species = NULL, trap = NULL,
             sex = "female", trapnight_min = 1, trapnight_max = NULL,
             separate_by = NULL)
```

| Argument        | Description                                                                                                       |
| --------------- | ----------------------------------------------------------------------------------------------------------------- |
| `collections`   | Collections data from `getArthroCollections()`                                                                    |
| `interval`      | Time interval: `"CollectionDate"`, `"Week"`, `"Biweek"`, or `"Month"`                                             |
| `agency`        | Optional character vector for filtering by agency code                                                            |
| `species`       | Optional species filter. Use `unique(collections$species_display_name)` to see options. Defaults to all species.  |
| `trap`          | Optional trap type filter. Use `unique(collections$trap_acronym)` to see options. Defaults to all trap types.     |
| `sex`           | Sex type filter. Use `unique(collections$sex_type)` to see options. Defaults to `"female"`.                       |
| `trapnight_min` | Minimum trap nights required for a collection to be included. Default is `1`.                                     |
| `trapnight_max` | Maximum trap nights allowed. Default is no restriction.                                                           |
| `separate_by`   | Group results by `"species"`, `"trap"`, `"agency"`, `"county"`, or `"spatial"`. Default `NULL` does not separate. |

**Example**

```r
getAbundance(
  sample_collections,
  interval    = "Biweek",
  species     = c("Cx tarsalis", "Cx pipiens"),
  trap        = "CO2",
  separate_by = "species"
) %>% head()
#>   Agency surv_year Biweek Count County     Species TrapEvents TrapType Abundance
#> 1     55      2020      1   142    ---  Cx pipiens         18      CO2      7.89
#> 2     55      2020      1    38    --- Cx tarsalis         18      CO2      2.11
#> 3     55      2020      2   209    ---  Cx pipiens         22      CO2      9.50
```

---

## getAbundanceAnomaly()

Compares the target year's abundance against the 5-year historical average for the same time period. Useful for identifying unusual activity relative to baseline conditions. Requires at least 5 years of prior data in your dataset.

$$\text{Anomaly (\%)} = \frac{\text{Current Year Abundance} - \text{5-Year Mean}}{\text{5-Year Mean}} \times 100$$

```r
getAbundanceAnomaly(collections, interval, target_year, agency = NULL,
                    species = NULL, trap = NULL, sex = "female",
                    trapnight_min = 1, trapnight_max = NULL, separate_by = NULL)
```

| Argument        | Description                                                                                                       |
| --------------- | ----------------------------------------------------------------------------------------------------------------- |
| `collections`   | Collections data from `getArthroCollections()`. Must span at least 6 years.                                       |
| `interval`      | Time interval: `"CollectionDate"`, `"Week"`, `"Biweek"`, or `"Month"`                                             |
| `target_year`   | Year to calculate anomaly for. Data must cover `target_year - 5` through `target_year`.                           |
| `agency`        | Optional character vector for filtering by agency code                                                            |
| `species`       | Optional species filter. Use `unique(collections$species_display_name)` to see options. Defaults to all species.  |
| `trap`          | Optional trap type filter. Use `unique(collections$trap_acronym)` to see options. Defaults to all trap types.     |
| `sex`           | Sex type filter. Defaults to `"female"`.                                                                          |
| `trapnight_min` | Minimum trap nights required for a collection to be included. Default is `1`.                                     |
| `trapnight_max` | Maximum trap nights allowed. Default is no restriction.                                                           |
| `separate_by`   | Group results by `"species"`, `"trap"`, `"agency"`, `"county"`, or `"spatial"`. Default `NULL` does not separate. |

**Example**

```r
getAbundanceAnomaly(
  sample_collections,
  interval    = "Biweek",
  target_year = 2020,
  species     = c("Cx tarsalis", "Cx pipiens"),
  trap        = "CO2",
  separate_by = "species"
) %>% head()
#>   Species Biweek Abundance_2020 Mean_2015_2019 Anomaly_Pct
#> 1  Cx pipiens      1          7.89           6.21       +27.1%
#> 2 Cx tarsalis      1          2.11           3.04       -30.6%
```

---

## getInfectionRate()

Estimates the arbovirus infection rate from pool testing data. Three estimation methods are available. Results are typically scaled per 1,000 mosquitoes for easier interpretation.

```r
getInfectionRate(pools, interval, target_year, target_disease, pt_estimate,
                 scale = 1000, agency = NULL, species = NULL, trap = NULL,
                 sex = NULL, separate_by = NULL)
```

| Argument         | Description                                                                                                           |
| ---------------- | --------------------------------------------------------------------------------------------------------------------- |
| `pools`          | Pools data from `getPools()`                                                                                          |
| `interval`       | Time interval: `"CollectionDate"`, `"Week"`, `"Biweek"`, or `"Month"`                                                 |
| `target_year`    | Year to calculate infection rate for                                                                                  |
| `target_disease` | Disease acronym (e.g., `"WNV"`). Use `unique(pools$target_acronym)` to see options.                                   |
| `pt_estimate`    | Estimation method: `"mle"` (maximum likelihood), `"bc-mle"` (bias-corrected MLE), or `"mir"` (minimum infection rate) |
| `scale`          | Result multiplier. Default is `1000` (rate per 1,000 mosquitoes).                                                     |
| `agency`         | Optional character vector for filtering by agency code                                                                |
| `species`        | Optional species filter. Use `unique(pools$species_display_name)` to see options. Defaults to all species.            |
| `trap`           | Optional trap type filter. Use `unique(pools$trap_acronym)` to see options. Defaults to all trap types.               |
| `sex`            | Optional sex type filter. Defaults to `"female"`.                                                                     |
| `separate_by`    | Group results by `"species"`, `"trap"`, or `"agency"`. Default `NULL` does not separate.                              |

**Estimation methods**

- **`mle`** — Maximum likelihood estimate. The standard approach for most analyses.
- **`bc-mle`** — Bias-corrected MLE. Recommended when pool sizes are large or infection rates are high.
- **`mir`** — Minimum infection rate. Assumes at most one positive per pool. Use when pool-level results are unavailable.

**Example**

```r
ir <- getInfectionRate(
  sample_pools,
  interval       = "Week",
  target_year    = 2020,
  target_disease = "WNV",
  pt_estimate    = "mle",
  scale          = 1000,
  species        = "Cx pipiens",
  trap           = c("CO2", "GRVD")
)

ir %>% head()
#>   Week Year   Species  Pools Positive    IR_MLE  LowerCI  UpperCI
#> 1   22 2020 Cx pipiens    12        1  2.31     0.06     12.87
#> 2   23 2020 Cx pipiens    15        0  0.00       NA        NA
#> 3   24 2020 Cx pipiens    18        2  3.74     0.45     13.51
```

---

## getVectorIndex()

The vector index combines abundance and infection rate to estimate the relative risk of arbovirus transmission in an area. Higher values indicate greater transmission risk.

$$\text{Vector Index} = \text{Abundance} \times \text{Infection Rate}$$

Collections and pools data must overlap in the years they cover.

```r
getVectorIndex(collections, pools, interval, target_disease, pt_estimate,
               scale = 1000, agency = NULL, species = NULL, trap = NULL,
               sex = "female", trapnight_min = 1, trapnight_max = NULL,
               separate_by = NULL)
```

| Argument         | Description                                                                                                      |
| ---------------- | ---------------------------------------------------------------------------------------------------------------- |
| `collections`    | Collections data from `getArthroCollections()`                                                                   |
| `pools`          | Pools data from `getPools()`. Must share overlapping years with collections.                                     |
| `interval`       | Time interval: `"CollectionDate"`, `"Week"`, `"Biweek"`, or `"Month"`                                            |
| `target_disease` | Disease acronym (e.g., `"WNV"`). Use `unique(pools$target_acronym)` to see options.                              |
| `pt_estimate`    | Infection rate estimation method: `"mle"`, `"bc-mle"`, or `"mir"`                                                |
| `scale`          | Result multiplier for infection rate. Default is `1000`.                                                         |
| `agency`         | Optional character vector for filtering by agency code                                                           |
| `species`        | Optional species filter. Use `unique(collections$species_display_name)` to see options. Defaults to all species. |
| `trap`           | Optional trap type filter. Use `unique(collections$trap_acronym)` to see options. Defaults to all trap types.    |
| `sex`            | Sex type filter. Defaults to `"female"`.                                                                         |
| `trapnight_min`  | Minimum trap nights required for a collection to be included. Default is `1`.                                    |
| `trapnight_max`  | Maximum trap nights allowed. Default is no restriction.                                                          |
| `separate_by`    | Group results by `"species"`, `"trap"`, or `"agency"`. Default `NULL` does not separate.                         |

**Example**

```r
getVectorIndex(
  sample_collections,
  sample_pools,
  interval       = "Biweek",
  target_disease = "WNV",
  pt_estimate    = "bc-mle",
  species        = "Cx tarsalis",
  trap           = "CO2"
) %>% head()
#>   Biweek Year   Species Abundance   IR_bcMLE VectorIndex
#> 1     22 2020 Cx tarsalis      4.2       1.85        0.0078
#> 2     23 2020 Cx tarsalis      6.1       0.00        0.0000
#> 3     24 2020 Cx tarsalis      5.8       3.74        0.0217
```

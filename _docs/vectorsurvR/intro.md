---
title: vectorsurvR Package
---

`vectorsurvR` is an R package for accessing, processing, and visualizing mosquito surveillance data from the [VectorSurv](https://vectorsurv.org/) platform. It replicates the calculations available in the VectorSurv Gateway and adds tools for generating publication-ready tables, charts, and maps directly in R.

You don't need to be an experienced programmer to use it — `vectorsurvR` provides straightforward functions to pull exactly the data you need from the API and makes it available as a starting point for calculations and visualizations.

A valid VectorSurv username and password is required to retrieve live data. Users without agency access can use the built-in sample datasets included with the package.

---

## Getting Started

### 1. Install R and RStudio

If you haven't already, download and install [R](https://cran.r-project.org/) and [RStudio](https://posit.co/downloads/).

### 2. Install vectorsurvR

**From CRAN (recommended):**

```r
install.packages("vectorsurvR")
```

**From GitHub (development version):**

```r
# Install devtools if not already installed
if (!require("devtools")) install.packages("devtools")

# Install vectorsurvR from GitHub
devtools::install_github("UCD-DART/vectorsurvR")
```

### 3. Load the package

```r
library(vectorsurvR)
```

### 4. Next Steps

- Watch the [Training Series on YouTube](https://www.youtube.com/watch?v=2BfMG0P6Ndc&list=PLbSUoxtSzuqQFhsquussQDNJdwt2-k1bh) for detailed walkthroughs
- Read the [GitHub User Guide](https://github.com/UCD-DART/vectorsurvR/tree/main)
- Browse the documentation sections below

---

## Documentation

| Section                                                                | Description                                                                    |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [Data Retrieval]({{ site.baseurl }}/docs/vectorsurvr/data-retrieval)   | Authenticate and pull collections, pools, sites, and spatial data from the API |
| [Data Processing]({{ site.baseurl }}/docs/vectorsurvr/data-processing) | Subset, filter, group, and reshape your data before analysis                   |
| [Calculations]({{ site.baseurl }}/docs/vectorsurvr/calculations)       | Abundance, abundance anomaly, infection rate, and vector index                 |
| [Tables]({{ site.baseurl }}/docs/vectorsurvr/tables)                   | Built-in table functions and styled output with kableExtra and DT              |
| [Charts & Plots]({{ site.baseurl }}/docs/vectorsurvr/charts-plots)     | Built-in plot functions and custom ggplot2 charts                              |
| [Mapping]({{ site.baseurl }}/docs/vectorsurvr/mapping)                 | Interactive and static species collection and pool testing maps                |

---

## Quick Start

```r
library(vectorsurvR)

# Authenticate
token <- getToken()

# Pull data
collections <- getArthroCollections(token, 2020, 2020, "mosquito", agency_ids = 55)
pools       <- getPools(token, 2020, 2020, "mosquito", agency_ids = 55)

# Calculate abundance
getAbundance(collections, interval = "Month", species = "Cx tarsalis")

# Map collections
plotSpeciesMap(token, target_year = 2020, interval = "Month", time_period = "June")

# Map pool testing results
plotPoolsMap(token, target_year = 2020, target_disease = "WNV",
             interval = "Month", time_period = "June")
```

---

## Sample Data

The package ships with two built-in datasets for learning and testing without a live API connection:

- `sample_collections` — example mosquito collection records
- `sample_pools` — example mosquito pool testing records

```r
head(sample_collections)
head(sample_pools)
```

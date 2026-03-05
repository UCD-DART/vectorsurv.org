---
title: Data Retrieval
---

The `vectorsurvR` package connects directly to the VectorSurv API to retrieve collections, pool testing, agency, site, and spatial data associated with your account. A valid VectorSurv username and password is required.

## Installation

Install the stable version from CRAN:

```r
install.packages("vectorsurvR")
```

Or install the development version from GitHub:

```r
devtools::install_github("UCD-DART/vectorsurvR")
```

Then load the package:

```r
library(vectorsurvR)
```

---

## getToken()

Authenticates your VectorSurv credentials and returns a token required by all data retrieval functions. You will be prompted to enter your Gateway username and password interactively.

```r
getToken()
```

**Example**

```r
token <- getToken()
```

> Your token expires after a set period. If you receive authentication errors, run `getToken()` again to refresh it.

---

## getArthroCollections()

Returns arthropod collection records for a specified year range and arthropod type. You can only retrieve data from agencies linked to your Gateway account.

```r
getArthroCollections(token, start_year, end_year, arthropod, agency_ids = NULL)
```

| Argument           | Description                                                                                        |
| ------------------ | -------------------------------------------------------------------------------------------------- |
| `token`            | Token from `getToken()`                                                                            |
| `start_year`       | First year of the retrieval range                                                                  |
| `end_year`         | Last year of the retrieval range                                                                   |
| `arthropod`        | Type of arthropod: `"mosquito"` or `"tick"`                                                        |
| `agency_ids`       | Optional. Numeric vector of agency IDs. Defaults to all agencies on your account.                  |
| `spatial_features` | Filter data by spatial feature                                                                     |
| `geocoded`         | Should city and county be calculated by collection long/lat instead of user input from site inform |

**Example**

```r
collections <- getArthroCollections(
  token,
  start_year = 2022,
  end_year   = 2023,
  arthropod  = "mosquito",
  agency_ids = 55
)
```

**Output:** A data frame with one row per collection record. Key columns include `collection_date`, `species_display_name`, `num_count`, `trap_acronym`, `site_code`, `collection_longitude`, and `collection_latitude`.

---

## getPools()

Returns pool testing records for a specified year range and arthropod type. Pools represent groups of mosquitoes submitted for disease testing.

```r
getPools(token, start_year, end_year, arthropod, agency_ids = NULL)
```

| Argument     | Description                                 |
| ------------ | ------------------------------------------- |
| `token`      | Token from `getToken()`                     |
| `start_year` | First year of the retrieval range           |
| `end_year`   | Last year of the retrieval range            |
| `arthropod`  | Type of arthropod: `"mosquito"` or `"tick"` |
| `agency_ids` | Optional. Numeric vector of agency IDs.     |

**Example**

```r
pools <- getPools(
  token,
  start_year = 2022,
  end_year   = 2023,
  arthropod  = "mosquito"
)
```

**Output:** A data frame with one row per pool record. Key columns include `collection_date`, `species_display_name`, `num_count`, `test_target_acronym`, `test_status_name`, `pool_longitude`, and `pool_latitude`.

---

## getAgency()

Returns agency profile data including spatial boundary polygons, if available. Boundaries can be edited through the VectorSurv Gateway.

```r
getAgency(token)
```

**Example**

```r
agency <- getAgency(token)
```

---

## getSites()

Returns site location information for your agency's monitoring network, including coordinates and site codes.

```r
getSites(token, agency_ids = NULL)
```

| Argument     | Description                             |
| ------------ | --------------------------------------- |
| `token`      | Token from `getToken()`                 |
| `agency_ids` | Optional. Numeric vector of agency IDs. |

---

## getSpatialFeatures()

Returns custom spatial regions (e.g., zones, districts) defined by your agency through the Gateway. Use the feature names returned here to filter maps and calculations by area.

```r
getSpatialFeatures(token, agency_ids = NULL)
```

| Argument     | Description                             |
| ------------ | --------------------------------------- |
| `token`      | Token from `getToken()`                 |
| `agency_ids` | Optional. Numeric vector of agency IDs. |

**Example**

```r
features <- getSpatialFeatures(token, agency_ids = 55)
# View available feature names
unique(features$name)
```

---

## Saving and Loading Data

We recommend saving retrieved data locally rather than re-querying the API every time you render a report. This speeds up rendering and keeps your workflow independent of network access.

```r
# Save to your working directory
write.csv(collections, file = "collections_22_23.csv", row.names = FALSE)

# Load it back in a future session
collections <- read.csv("collections_22_23.csv")
```

---

## Sample Data

The package includes two built-in datasets for learning and testing without a live API connection:

- `sample_collections` — example mosquito collection records
- `sample_pools` — example mosquito pool testing records

```r
library(vectorsurvR)

head(sample_collections)
head(sample_pools)
```

These datasets are used throughout the documentation examples.

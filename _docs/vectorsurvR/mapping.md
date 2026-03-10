---
title: Mapping
---

The mapping functions in `vectorsurvR` generate interactive Leaflet maps of collection and pool testing data. Maps include toggleable layers for monitoring sites, agency boundaries, and custom spatial features.

> **HTML vs. static output:** Interactive Leaflet maps cannot be embedded in Word or PDF files. When knitting to those formats, set `html = FALSE` to automatically capture a screenshot of the map instead. This requires a one-time setup — see [Static Output Setup](#static-output-setup) below.

---

## plotSpeciesMap()

Creates an interactive map displaying mosquito collection data for a target year. Collection locations are colored by species. Single-species sites appear as colored circles sized proportionally to mosquito count. Sites with multiple species display pie charts showing relative species composition.

```r
plotSpeciesMap(token, target_year, species = NULL, trap = NULL, agency_ids = NULL,
               interval = NULL, time_period = NULL, basemap = "Topographic",
               spatial_features = NULL, html = TRUE, height = 400)
```

| Argument | Description |
|---|---|
| `token` | Token from `getToken()` |
| `target_year` | Year to display collection data for |
| `species` | Optional species filter. Use `unique(collections$species_display_name)`. |
| `trap` | Optional trap type filter. Use `unique(collections$trap_acronym)`. |
| `agency_ids` | Optional agency filter |
| `interval` | Time interval for filtering: `"Month"`, `"Week"`, or `"Biweek"`. If `NULL`, all data for the year is shown. |
| `time_period` | Specific period within the interval (e.g., `"July"` for Month, `5` for Week 5). |
| `basemap` | Background map style: `"Topographic"` (default), `"Satellite"`, or `"Terrain"` |
| `spatial_features` | Optional vector of spatial feature names to overlay as polygons. Use `getSpatialFeatures()` to see available options. |
| `html` | Logical. `TRUE` (default) returns an interactive map. Set to `FALSE` when knitting to Word or PDF. |
| `height` | Pixel height of the screenshot when `html = FALSE`. Default is `400`. |

**Map layers**

- **Agency Boundaries** — dashed grey polygon showing agency jurisdiction
- **Spatial Features** — blue polygons for custom zones or regions (if specified)
- **Monitoring Sites** — active sites in black, inactive sites in grey
- **Collections** — species markers sized by count, colored by species; multi-species locations show pie charts

**Examples**

```r
# Basic map for a specific month
plotSpeciesMap(
  token       = token,
  target_year = 2024,
  interval    = "Month",
  time_period = "September",
  agency_ids  = 55
)

# Filter by species and trap type
plotSpeciesMap(
  token       = token,
  target_year = 2024,
  species     = c("Cx tarsalis", "Cx pipiens"),
  trap        = "CO2",
  agency_ids  = 55
)

# With spatial features overlay
plotSpeciesMap(
  token            = token,
  target_year      = 2024,
  interval         = "Month",
  time_period      = "July",
  species          = "Ae aegypti",
  spatial_features = "ZONES=31",
  agency_ids       = 55
)

# Static output for Word or PDF
plotSpeciesMap(
  token       = token,
  target_year = 2024,
  interval    = "Month",
  time_period = "September",
  agency_ids  = 55,
  html        = FALSE,
  height      = 500
)
```

---

## plotPoolsMap()

Creates an interactive map displaying mosquito pool testing results for a target year. Positive pools are marked with red borders and colored by species; negative pools appear in blue. Marker size reflects the number of pools tested at each location. Sites with multiple positive species show pie charts.

```r
plotPoolsMap(token, target_year, target_disease = NULL, species = NULL,
             trap = NULL, agency_ids = NULL, interval = "Month",
             time_period = NULL, basemap = "Topographic",
             spatial_features = NULL, show_agency_boundaries = TRUE,
             html = TRUE, height = 400)
```

| Argument | Description |
|---|---|
| `token` | Token from `getToken()` |
| `target_year` | Year to display pool testing data for |
| `target_disease` | Optional disease filter (e.g., `"WNV"`). Use `unique(pools$target_acronym)`. |
| `species` | Optional species filter. Use `unique(pools$species_display_name)`. |
| `trap` | Optional trap type filter. Use `unique(pools$trap_acronym)`. |
| `agency_ids` | Optional agency filter |
| `interval` | Time interval for filtering: `"Month"` (default), `"Week"`, `"Biweek"`, or `"Year"` |
| `time_period` | Specific period within the interval (e.g., `"July"` for Month, `"Week 5"` for Week). |
| `basemap` | Background map style: `"Topographic"` (default), `"Satellite"`, or `"Terrain"` |
| `spatial_features` | Optional vector of spatial feature names to overlay as polygons. |
| `show_agency_boundaries` | Logical. Whether to display agency boundary polygons. Default is `TRUE`. |
| `html` | Logical. `TRUE` (default) returns an interactive map. Set to `FALSE` when knitting to Word or PDF. |
| `height` | Pixel height of the screenshot when `html = FALSE`. Default is `400`. |

**Examples**

```r
# WNV pools for a specific month
plotPoolsMap(
  token          = token,
  target_year    = 2024,
  target_disease = "WNV",
  interval       = "Month",
  time_period    = "July",
  agency_ids     = 55
)

# Filter by species and trap type
plotPoolsMap(
  token          = token,
  target_year    = 2024,
  target_disease = "WNV",
  species        = c("Cx tarsalis", "Cx pipiens"),
  trap           = "CO2",
  agency_ids     = 55
)

# Static output for Word or PDF
plotPoolsMap(
  token          = token,
  target_year    = 2024,
  target_disease = "WNV",
  interval       = "Month",
  time_period    = "September",
  agency_ids     = 55,
  html           = FALSE,
  height         = 500
)
```

---

## Static Output Setup

Interactive maps require a screenshot to be embedded in Word or PDF reports. This is handled automatically when `html = FALSE`, but requires a one-time setup:

```r
install.packages(c("webshot2", "htmlwidgets"))
webshot2::install_chromote()
```

Run these once in your R console. After setup, simply pass `html = FALSE` to either map function and the screenshot is generated automatically on knit.

> If your screenshot appears blank or grey, the browser may not have had enough time to load the map tiles. This is handled internally with a 3-second delay, but complex maps with many markers may occasionally need more time. If this happens, [contact support]({{ site.baseurl }}/docs/contact) or file an issue on the [GitHub repository](https://github.com/UCD-DART/vectorsurvR).

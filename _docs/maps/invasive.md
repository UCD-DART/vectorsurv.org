---
title: Invasive Map
---

### Overview

The [VectorSurv invasive map](https://maps.vectorsurv.org/invasive) shows the spread of invasive mosquito species over time, based on collection data submitted to VectorSurv.

### Map

**Update frequency:** The map is refreshed once daily at midnight Pacific Time and does not display real-time data.

Collection events are aggregated spatially into regions on the map, each of which represents the intersection of a census county subdivision and the boundary VectorSurv has on record for the member agency covering that area. The color in each region corresponds to the known presence or absence of the species:

- Red indicates that the selected species was detected within the selected timeframe. Species complexes are not counted as detections. (For instance, Cx pipiens + quinquefasciatus collections do not count as Cx quinquefasciatus collections).
- Gray indicates that at least one collection occurred within the selected timeframe, but no mosquitoes of the selected species were found.
- Light gray indaicates that no collections occurred within the selected timeframe.

The following collection events are included on the map:

- Any collection with at least 1 specimen that exactly matches any of the invasive species options.
- Any other collection using an eligible trap.

#### Eligible traps

- American Biophysics Corporation (ABC) trap
- BG Sentinel
- Carbon dioxide baited trap
- CDC Autocidal Gravid Ovitrap (counts)
- CDC Autocidal Gravid Ovitrap (presence/absence)
- CDC miniature light trap
- CDC-style Gravid Trap
- Collection Bottle Rotator Trap
- EVS (Encephalitis Vector Survey) trap
- Frommer Updraft Gravid Trap
- Gravid trap
- Modified CDC Autocidal Gravid Ovitrap (counts)
- New Jersey light trap
- Oviposition Trap (counts)
- Oviposition Trap (presence/absence)
- Reiter-Cummings Gravid Trap

### Chart

Clicking any region replaces the tutorial card with a chart. Chart items can be shown or hidden by clicking the legend below the chart.

#### Bar Chart

The chart uses a stacked bar chart to show collection events over time, with time on the horizontal axis and the number of collection events on the vertical axis.

Each bar comprises up to two colored segments:

- Red — collections containing the selected species
- Gray — collections not containing the selected species

Charted collection events are aggregated based on the selected timeframe:

- By week when the selected timeframe is 2 years or less
- By month when the timeframe is between 2 and 5 years
- By quarter when the timeframe exceeds 5 years

#### Projected growth line:

The overlaid projected growth line, available only for certain species, is a function of temperature. VectorSurv uses NLDAS temperature data.

### Summary Table

Clicking any region displays a summary table section below the chart. The summary includes:

#### Regional Information

- County
- County subdivision
- Member agency covering the area
- Member agency website

#### Species Information

A table showing, for each species listed below:

- **Total detections** in the selected timeframe
- **Total detections** all time
- **Date first found**
- **Date last found**

Species shown include:

- Aedes aegypti
- Aedes albopictus
- Aedes notoscriptus
- The species currently selected

The first three species are always included. They are considered the invasive species of greatest concern across the United States due to their status as Dengue/Chikungunya/Zika virus vectors.

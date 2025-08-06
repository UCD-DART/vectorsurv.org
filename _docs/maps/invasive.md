---
title: VectorSurv Invasive Map
---

### Overview

The [VectorSurv invasive map](https://maps.vectorsurv.org/invasive) shows the spread of invasive mosquito species over time, based on collection data submitted to VectorSurv.

### Mapped data aggregation

The spread of invasive mosquitoes is determined by analyzing mosquito collection events entered into VectorSurv. Collection events are aggregated spatially into regions on the map, each of which represents the intersection of a census county subdivision and the boundary VectorSurv has on record for the member agency covering that area. The following collection events are included on the map:

- Any collection with at least 1 specimen that exactly matches any of the invasive species options. Species complexes are not counted as detections. (For instance, Cx pipiens + quinquefasciatus collections do not count as Cx quinquefasciatus collections).
- Any other collection with the following trap types: "American Biophysics Corporation (ABC) trap", "BG Sentinel", "Carbon dioxide baited trap", "CDC Autocidal Gravid Ovitrap (counts)", "CDC Autocidal Gravid Ovitrap (presence/absence)", "CDC miniature light trap", "CDC-style Gravid Trap", "Collection Bottle Rotator Trap", "EVS (Encephalitis Vector Survey) trap", "Frommer Updraft Gravid Trap", "Gravid trap", "Modified CDC Autocidal Gravid Ovitrap (counts)", "New Jersey light trap", "Oviposition Trap (counts)", "Oviposition Trap (presence/absence)", "Reiter-Cummings Gravid Trap".

### Bar chart

On the bar chart, collection events are aggregated:

- By week when the selected timeframe is 2 years or less
- By month when the timeframe is between 2 and 5 years
- By quarter when the timeframe exceeds 5 years

### Projected growth line:

The overlaid projected growth line, available only for certain species, is a function of temperature. VectorSurv uses NLDAS temperature data.

---
title: Invasive Map
---

### Overview

The [VectorSurv invasive map](https://maps.vectorsurv.org/invasive) shows the spread of invasive mosquito species over time, based on collection data submitted to VectorSurv.

![Map on the left and chart plus summary on the right. The map is centered on California and shows red, gray, and light gray regions. The chart is a stacked bar chart with a line overlay.](/assets/images/docs/invasive-map.png)

### Map

_Update frequency:_ The map is refreshed once daily at midnight Pacific Time and may not display real-time data.

Collection events are aggregated spatially into regions on the map, each of which represents the intersection of a census county subdivision and the boundary VectorSurv has on record for the member agency covering that area. The color in each region corresponds to the known presence or absence of the species:

- **Red** indicates that the selected species was detected within the selected timeframe. Species complexes are not counted as detections. (For instance, Cx pipiens + quinquefasciatus collections do not count as _Cx quinquefasciatus_ collections.)

![Map showing regions in red where the selected species was detected.](/assets/images/docs/invasive-map-detections.png)

- **Gray** indicates that at least one collection occurred within the selected timeframe, but no mosquitoes of the selected species were found.

![Map showing regions in gray where collections occurred but the selected species was not found.](/assets/images/docs/invasive-map-no-detections.png)

- **Light gray** indicates that no collections occurred within the selected timeframe.

![Map showing regions in light gray where no applicable collections occurred.](/assets/images/docs/invasive-map-no-surv.png)

The following collection events are included on the map:

- Any collection with at least one specimen that exactly matches any of the invasive species options
- Any other collection using an eligible trap

#### Eligible Traps

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

![A bar chart with time on the x-axis and collections on the y-axis. The bars are a combination of gray and red, with a line chart overlaid.](/assets/images/docs/invasive-map-bar-chart.png)

#### Bar Chart

The chart uses a stacked bar format to show collection events over time, with time on the horizontal axis and the number of collection events on the vertical axis.

Each bar comprises up to two colored segments:

- **Red** — collections containing the selected species
- **Gray** — collections not containing the selected species

Mousing over any bar brings up a tooltip with detailed counts.

Based on the selected timeframe, charted collection events are aggregated:

- By week when the selected timeframe is 2 years or less
- By month when the timeframe is between 2 and 5 years
- By quarter when the timeframe exceeds 5 years

#### Projected Growth Line

The overlaid projected growth line, which is available only for certain species, is a function of temperature. VectorSurv uses NLDAS temperature data.

### Summary Table

Clicking any region displays a summary table section below the chart.

![Summary with regional details above a table showing counts and dates of invasive species detections in the selected region.](/assets/images/docs/invasive-map-summary.png)

The summary includes:

#### Regional Information

- County
- County subdivision
- Member agency covering the area
- Member agency website

#### Species Information

- _Total detections_ in the selected timeframe
- _Total detections_ all time
- _Date first found_
- _Date last found_

Species shown include:

- _Aedes aegypti_
- _Aedes albopictus_
- _Aedes notoscriptus_
- The species currently selected

The first three species are always included. They are considered the invasive species of greatest concern across the United States due to their status as Dengue/Chikungunya/Zika virus vectors.

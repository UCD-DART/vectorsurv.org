---
title: Sample Reports
permalink: /docs/vectorsurvr/sample-reports/
---

Download these R Markdown templates to get started quickly. Each report is pre-configured with a user configuration block at the top — update your agency ID, year, and week range, then knit to HTML, Word, or PDF.

### [Mosquito Abundance Report]({{ site.baseurl }}/assets/reports/abundance_report.Rmd)

A weekly surveillance summary covering mosquito abundance, species composition, 5-year trend comparisons, and collection maps. Requires collections data only.

### [Arbovirus Disease Activity Report]({{ site.baseurl }}/assets/reports/disease_activity_report.Rmd)

A pool testing summary covering all diseases, with per-disease infection rate tables, positive pool detail, and pool testing maps. Requires pools data only.

### [Combined Abundance & WNV Report]({{ site.baseurl }}/assets/reports/wnv_abundance_report.Rmd)

A full surveillance report combining mosquito abundance and West Nile Virus activity into a single document. Requires both collections and pools data.

---

**One-time setup required before knitting any report:**

```r
install.packages(c("vectorsurvR", "dplyr", "ggplot2", "lubridate", "kableExtra"))
```

For map output in Word or PDF, also run:

```r
install.packages(c("webshot2", "htmlwidgets"))
webshot2::install_chromote()
```

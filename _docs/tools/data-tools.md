---
title: Data Tools
gateway-url: https://gateway.vectorsurv.org/core/ppf/menu/path/81
youtube-url: https://youtu.be/yO_04FFS4R4
---

Quickly import and export data.

## Data Import

Import data only for your current agency. You can change agencies using the **Current Agency** box on the righthand side of the screen.
![Current Agency Box]({{ site.baseurl }}/assets/images/docs/current-agency.PNG)

- **Import Type**: What type of data are you importing? Only one selection is possible.
- **File**: Choose the file to upload from your desktop. Note that the file must be one of Microsoft Excel (.xls or .xlsx) or Comma Separated Values (.csv).
  - Note that the file must follow the import rules for the specific _Import Type_ being used in order for the import to be successful. Import specifications can be found by following the links below.

> ### General Import Specifications
>
> - [Rules governing the structures and formats of the various import types.](https://ucdavis.app.box.com/v/VS-Gateway-Import-Specs)
>
> ### Arthro Collections - Formatted Specifications
>
> **Specifications and template files specific to the Arthro Collection - Formatted import type.**
>
> - [Generic Sample](https://gateway.vectorsurv.org//doc/arthro_collection_formatted/generic/generic.zip)
> - [California Sample](https://gateway.vectorsurv.org//doc/arthro_collection_formatted/CA/CA.zip)
>
> ### Web Service Documentation
>
> - [Instructions detailing the Import Web service and how to use the service from local applications.](https://trac.vectorsurv.org/gateway/wiki/ImportWebService)

These links can also be found in the information panel at the bottom of the [Data Import page](https://gateway.vectorsurv.org/core/ppf/import).

## Export Data

Select the **Export Type** to choose which data you wish to export. Export format preferences can be modified under _Documents_ on the [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences) page.

## Aggregate Reports

Quickly generate reports from your agency or from multiple agencies to compare arbovirus activity.

- **Agency**: Choose the agency(ies) you wish to generage a report for. Multiple agencies can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values.
- **Disease Week**: Select the epi-week and year for the data if you are interested in a specific week. Choosing a date range here will autofill the **From/To** sections below.
- **From/To**: Manually enter the start/end dates for the data. The date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences). The subsequent boxes are a time field; if not provided, the hour is assumed to be 0 of 00:00.
- **Report**: Use the checkboxes to select which type of report(s) will be generated. If there are results in the provided date range for the selected agencies, you can view and download the resulting tables.

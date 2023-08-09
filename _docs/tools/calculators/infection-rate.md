---
title: Pool Infection Rate
gateway-url: https://gateway.vectorsurv.org/arthro/ppf/pool_infection_calc
---

The pool infection rate calculator estimates the arbovirus infection rate based on testing pools of mosquitoes. This calculator is intended to reproduce [statistical methods implemented by CDC](https://www.cdc.gov/westnile/resourcepages/mosqSurvSoft.html) for estimation of infection prevalence from pooled samples.

## Fields

- **Peer Agency**: In addition to calculations for your own agency (the default), this selection allows you to choose other agencies for which you wish to calculate an infection rate. Multiple agencies can be selected by using the _CTRL/CMD_, or _SHIFT_ keys while selecting values. This allows you to compare results for your agency to those of neighboring agencies. Note that calculations for other agencies are possible only for the the entire agency. If the _Treat each selected agency independently_ box is checked, the rates will be calculated separately for each agency (ignored if only one agency is selected). If left unchecked, the infection rate will be aggregated for all selected agencies. Your agency is always treated separately.

- **Date Period**: Specify the time period for which you wish to calculate an infection rate. You can manually select a date range with the date format specified on your [Account Preferences]({{ site.baseur1 }}/docs/settings/account-preferences) page, or choose a specific week or month within a year. If calculating for a month, there is a box to specify whether to use half-months instead of full-months. If this box is checked, each month will be divided into two parts, days 1-15 and days 16 to the last day of the month (28, 29, 30, or 31). 

  ![Date period field]({{ site.baseur1 }}/assets/images/docs/date-range-infection-rate.PNG)
- **# of Date Periods**: Must be at least 1 to make a calculation. If this number = 1 (the default), calculations will be performed only for the specified date period. If this number is > 1, the infection rate will calculated for the specified number of date periods going *backward* in time from the specified date period. Intervals of prior date periods match those of the ***Date Period*** defined above.
Example: If you define a manual date period of 4 days and set the number of date periods = 2, the calculator will estimate the infection rate separately for the selected 4-day period and for the 4-day period immediately preceding the start date of your range.
- **Spatial Filter**: This feature allows you to filter results within your agency by geographic location. You can use the *Feature* tab to select one or more pre-defined features (i.e., spatial areas) from the [Spatial Features]({{ site.baseurl }}/docs/tools/spatial-tools) page. ![Polygon example]({{ site.baseur1 }}/assets/images/docs/spatial-feature-tools.PNG) Alternatively, you can filter by [site group]({{ site.baseur1 }}/docs/site/site-group), region (e.g., county), or one or more specific sites. For these filters, multiple values can be selected by using the _CTRL/CMD_, or _SHIFT_ keys while selecting values. If the _Treat each selected filter independently_ box is checked, the infection rate will be stratified by spatial filter, otherwise the rate will be aggregated for the selection. If the "All Available..." option is selected or no feature polygon is chosen, calculations will not use spatial filters.
- **Target/Virus**: The pathogen for which you wish to estimate the infection rate.
- **Species**: Here you can choose whether to look at the infection rate for all species or selected species of interest. The *Species Group* tab allows for selection of certain pre-defined species or groups of species. Multiple species can be selected by using the _CTRL/CMD_, or _SHIFT_ keys while selecting values. If the _Treat each selected species independently_ box is checked, the infection rate will be stratified by species, otherwise the rate will be aggregated for all selected species.
- **Sex/Condition**: Almost all testing and infection rate calculations will focus on females in various gonotrophic conditions (i.e., unfed, bloodfed, or gravid, or mixed), but other options are also possible if it is necessary to perform calculations for males, unknown sex, eggs, larvae, and pupae. Multiple values can be selected by using the _CTRL/CMD_, or _SHIFT_ keys while selecting values, and checking the _Treat each selected sex/condition individually_ box will stratify the infection rate by the selected values.
- **Trap Type**: Filter the results by the trap type used for the collection. This is helpful to ensure that results are comparable over time and/or across agencies. Similar to **Sex/Condition**, multiple trap types can be selected by using the _CTRL/CMD_, or _SHIFT_ keys while selecting values, and checking the _Treat each selected trap type individually_ box will stratify the infection rate by the selected traps.
- **Point Estimate**: The type of infection rate to calculate. The bias-corrected maximum-likelihood estimate (MLE) will be appropriate for most situations, but you can also choose to calculate the MLE or MIR.
- **Confidence Interval**: Select the confidence level for the estimate. This is generally left at 95%.
- **Scale**: The value by which to scale the infection rate and confidence interval. The default is 1,000, which estimates the infection rate per 1,000 female mosquitoes. 100 could be used for calculating a percentage.

## Results

The **# of Calculations** provides a general indication of the number of calculations that will be performed based on the combination of choices made for the filters. If many filters have been applied, this number can become quite large. If no additional filters were applied, the infection rate will be estimated as a single calculation for the specified time interval.

The resulting table is downloadable, and you also have the option to view a time series graph (one graph per stratification) comparing the infection rate over the date periods (if more than 1).

If the calculator times out due to a very large number of calculations requested, try again with a smaller number of calculations.

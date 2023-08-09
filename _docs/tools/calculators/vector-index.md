---
title: Vector Index
gateway-url: https://gateway.vectorsurv.org/arthro/ppf/vector_index_calc
---

The vector index is the relative abundance of infected mosquitoes and is a way to quickly estimate the risk of arbovirus transmission in an area. Vector index is the product of the abundance and infection rate for a given time interval: 

$$VI = \text{Abundance * Infection Rate}$$

## Fields

- **Peer Agency**: Your agency is automatically selected. You may choose any additional peer agencies for which you wish to calculate vector index. This can be used to compare your data to neighboring districts. Multiple peer agencies can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values. If the _Treat each selected agency independently_ box is checked, the vector index will be stratified by peer agency (this is ignored if only one agency is selected). If left unchecked, vector index will be aggregated for all selected peer agencies. Your agency will always be treated separately. 
- **Year**: This is the year for which you wish to calculate a vector index. When calculating the [abundance anomaly]({{ site.baseur1 }}/docs/tools/calculators/anomaly) component, this year's abundance at the desired time interval will be compared to the average abundance from the previous 5 years.
- **Time Interval**: How frequently should the vector index components be calculated? There are several built-in options, or you can manually specify a date range within the selected year. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
- **Spatial Filter**: This feature allows you to filter results within your agency. You can draw a polygon on the map using the feature tab, or include a previously saved feature from the [Spatial Features]({{ site.baseurl }}/docs/tools/spatial-tools) page. ![Polygon example]({{ site.baseur1 }}/assets/images/docs/spatial-feature-tools.PNG) Alternatively, you can filter by [site group]({{ site.baseur1 }}/docs/site/site-group), region (determined when creating a [new site]({{ site.baseur1 }}/docs/site)), or specific site. For these filters, multiple values can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values. If the _Treat each selected filter independently_ box is checked, the vector index will be stratified by spatial filter, otherwise it will be aggregated for the selection. If the "All Available..." option is selected or no feature polygon(s) is provided, any calculation(s) will not use spatial filters. Spatial features only apply to your agency; you cannot calculate abundance anomaly within spatial features for peer agencies. Instead, abundance anomalies are calculated for whole peer agencies.
- **Target/Virus**: The pathogen for which you wish to estimate the [pool infection rate]({{ site.baseur1 }}/docs/tools/calculators/infection-rate) component.
- **Species**: Here you can choose whether to look at the vector index for all species or selected species of interest. Multiple species can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values. If the _Treat each selected species independently_ box is checked, the vector index will be stratified by species, otherwise it will be aggregated for all selected species.
- **Sex/Condition**: Typically, females of various conditions are of interest when calculating the vector index, but you could also examine males, unknown sex, eggs, larvae, and pupae. Multiple values can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values, and checking the _Treat each selected sex/condition individually_ box will stratify the vector index by the selected values.
- **Trap Type**: Filter the results by the trap type used for the collection. This is helpful to ensure that results are comparable over time and/or across agencies. Similar to **Sex/Condition**, multiple trap types can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values, and checking the _Treat each selected trap type individually_ box will stratify the vector index by the selected traps.
- **Trap Night Restrictions**: You can further restrict the collections used to calculate the vector index by the number of trap nights a trap was set for.
- **Point Estimate**: The infection rate estimation method. The bias-corrected MLE will be appropriate for most situations, but you can also choose to use the MLE or MIR methods.

True infection rate is calculated as (# Infected arthropods/total arthropods in pool)*1000. In most cases, arthropods are not tested for diseases individually and the actual number of disease positive arthropods in a positive pool remains unknown. Fortunately, infection rates can be estimated using the following methods.

 - **MIR**: Minimum Infection Rate makes the assumptions that there is only one positive mosquito in an infected pool of at least 1000 arthropods. MIR is not always a reliable estimate of IR as it is possible for multiple positive arthropods to be present in a positive pool and pools often contain fewer than 1000 arthropods. MIR is calculated as
$$\text{MIR} =  \frac{\text{Number Positive Pools}} {\text{Total Number Individuals}}  * 1000$$
 - **MLE**: Maximum Likelihood Estimate Infection Rate is estimated using a binomial model to approximate the infection rate based on the available data. The spread and center of the data is used to derive confidence intervals. Confidence intervals can be interpreted as the range of possible estimates for infection rate and a 95% confidence interval indicates you can be 95% confident that the true infection rate is within the given interval. The wider the confidence interval, the greater the uncertainty about the point estimate.

 - **Bias-Corrected MLE**: The standard MLE can have significant bias depending on the quantity and quality of available data. The bias-corrected MLE seeks to reduce this bias and is the recommended point estimate when sample size is small. The bias-corrected MLE will be appropriate for most situations.


## Results

The **# of Calculations** indicator shows how many calculations will be performed based on the stratifications (checkboxes) that have been selected. If none of the boxes were checked, the vector index at the desired time interval will be aggregated to a single calculation. The resulting table showing the vector abundance for the selected year and the previous 5 years is downloadable. You also have the option to view a time series graph comparing the vector index at the selected time interval.

- **Vector Index (VI)**: Vector index result which is calculated by multiplying the infection rate by the abundance for each interval
- **Abundance**: Abundance is defined as the total number of specie collections divided by the total number of trapping opportunities for a given time interval
- **Infection Rate**: Infection rate point estimate calculated from the selected method
- **Count**: The interval sum of arthropods used in the abundance calculation.
- **Trap Nights**: The total trapping opportunities for the time interval. This value is the interval sum of the number of traps set for a collection times the number of nights the traps were run for the trap types of interest.  For example, if a week contained two collections with CO2 traps: 5 traps run for 4 nights and 2 traps run for 1 night, the Trap Nights for that week would be:$(5 * 4) + (2 * 1) = 22$ regardless if the species of interest was found at either collections' traps. Essentially, trapping opportunities is dependent on the trap type.

- **Pools**: The total number of pools used in the calculation for infection rate

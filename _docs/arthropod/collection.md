---
title: New Collection
gateway-url: https://gateway.vectorsurv.org/arthro/ppf/collection
youtube-url: https://youtu.be/cZAveMzkIvU
---

Collections are the records of arthropod population data through the placement of traps.

## Fields

- **Trap Type**: The type of trap placed in the field. The list of traps in the dropdown can be adjusted through the [trap types configuration]({{ site.baseurl }}/docs/arthropod/trap-types) page.
- **Lure Type**: The types of lure(s) used with the trap if any. Multiple values can be selected by using _CTRL/CMD/SHIFT_ keys while selecting values. _Unspecified_ and _None_ can only be selected individually.
- **Collection Date**: The date the trap was picked up. If a trap was left for multiple nights, enter the last day the trap was in the field. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences). A date needs to be selected before you can choose at trap site.
- **# of Traps**: The number of unique traps in operation at one site.
- **# of Nights/Trap**: The number of nights a trap was in the field. Minimum of 1. If a trap was placed and collected in the same day, enter 1. If a trap was placed and collected the next day, enter 1.
- **Trap(s) at Site**: The [site]({{ site.baseurl }}/docs/site/) where a trap was placed. Start typing in any part of the site code or name and the dropdown will filter the sites to that text. Once a site is selected, the trap can be adjusted up to 400m away indicated by the circle.  
  ![Collection Site Map]({{ site.baseurl }}/assets/images/docs/collection_site_radius.png)  
  If a collection is made at a location that is not a normal trapping location, the 0 site code (length varies based on state settings) can be used for a 1 time trapping event. Select the 0 code and the marker on the map can be moved or geolocated to any location.
- **Coordinate Precision**: Used to specify whether or not a trap is marked exactly. This will be carried over from when the site was saved. Should be kept as _Exact_ for most data; this is to specify historical data that might not be as accurate as modern data.
- **Identified By**: The person who identified the arthropods in this trap.
- **Trap(s) ran with no problems?**: If checked, the trap used for this collection is considered to have NOT experienced any mechanical failures, i.e. fan broke, dead battery, etc. Uncheck if the trap experienced a problem during the trapping period.
- **Comments**: Use this section to note anything other users should know about the collection, including the reason(s) for trap failure, for example.
- **Count of Species**: A listing of arthropods found in the trap. It is not necessary to mark 0 counts as that is assumed when left blank or absent from the form.
  - **Species**: Start typing in the species and the field will autocomplete.
  - **M**: Males.
  - **F - Mixed**: Females of unknown status. Generally all females will be marked here. If females are marked as mixed, the following 3 columns are disabled.
  - **F - Unfed**: Females that were known to be unfed.
  - **F - Bloodfed**: Females known to be bloodfed.
  - **F - Gravid**: Females known to be gravid.
  - **Σ F**: The total of all _female_ columns. Data cannot be entered here, this column is for your convenience.
  - **Unknown Sex**: The arthropod's sex cannot be identified.
  - **Eggs**: Eggs collected.
  - **Larvae**: Larvae collected.
  - **Pupae**: Pupae collected.

## Pools

Optionally, a pool for arbovirus testing can be entered through the collection page. This links the pool to the collection that the pool originated from.

- **Pool #**: A numeric identifier for the pool. Pool numbers have to be unique per agency per year. Normally you would start at 1 and increment throughout the year but the exact numbering scheme is up to you. Available numbers for your agency are shown in the **Open 20xx Pool #s** box on the righthand side of the page.
  ![Open Pool #s box]({{ site.baseurl }}/assets/images/docs/open_pools.PNG)
- **Other Sites**: List other Site Codes that contributed arthropods to this pool separated by commas. Ex: 001001,001002,001003.  
  To specify the number of specimens contributed by a site, place the quantity after the site code wrapped by parentheses. Ex: 001001(12),001002,001003(2).
- **Species**: The species that make up this pool.
- **Sex/Condition**: The sex/condition of the arthropods in this pool.
- **# in Pool**: The total number of specimens in this pool. If this pool has specimen from more than one site (denoted in the Other Sites column), the number of specimens from the primary site (Site Code column) will be determined from this value.
- **Comments**: Any accompanying comments.

## KDR Resistance Testing (California ONLY)

If an _Ae. aegypti_ specimen is collected, a checkbox will appear to mark the mosquitoes to be tested by CDPH for KDR Testing.
![Collections KDR Testing]({{ site.baseurl }}/assets/images/docs/kdr_testing_input.png)  
Select **Test for Resistance** and a box will appear below with each individual mosquito. Click on the rows that you will send to CDPH, clicking on **Include?** in the header will mark all mosquitoes to be sent. The **Tube #** column should automatically populate for any rows that you mark down. You must select the status the mosquito was collected in the **Collected Live** column. When ready to send to CDPH, create a KDR Tube Submission.

---
title: New Pools (Legacy)
try-new: https://gateway.vectorsurv.org/v5/mosquito/pool/pool
gateway-url: https://gateway.vectorsurv.org/arthro/ppf/pool
youtube-url: https://youtu.be/cZAveMzkIvU
---

Pool submissions are records of groups of mosquitoes sent to be tested for arboviruses.

This page serves the same purpose as the optional pool entry form on the [new collection]({{ site.baseurl }}/docs/arthropod/collection) page. Pools entered here can be linked back to a specific collection from the [Collection Management]({{ site.baseurl }}/docs/arthropod/collection-manage) page. One or the other should be used to submit a single pool.

## Fields

- **Pool #**: A numeric identifier for the pool. Pool numbers have to be unique per agency per year. Normally you would start at 1 and increment throughout the year but the exact numbering scheme is up to you. Available numbers for your agency are shown in the **Open 20xx Pool #s** box on the righthand side of the page.
  ![Open Pool #s box]({{ site.baseurl }}/assets/images/docs/open_pools.PNG)
- **Site Code**: The numeric code for the primary site from which the arthropods were collected. Note that this feature does not allow filtering by the site name.
- **Other Sites**: List other Site Codes that contributed arthropods to this pool separated by commas. Ex: 001001,001002,001003.  
  To specify the number of specimens contributed by a site, place the quantity after the site code wrapped by parentheses. Ex: 001001(12),001002,001003(2).
- **Trap Type**: The type of trap that was used for the collection. The list of traps in the dropdown can be adjusted through the [trap types configuration]({{ site.baseurl }}/docs/arthropod/trap-types) page.
- **Lure(s)**: The types of lure(s) used with the trap, if any. Multiple values can be selected by using _CTRL/CMD/SHIFT_ keys while selecting values. _Unspecified_ and _None_ can only be selected individually.
- **Collection Date**: The date the trap was picked up. If a trap was left for multiple nights, enter the last day the trap was in the field. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences). If the _Enable calendar for dates_ box is checked below the table, clicking the **Collection Date** field will pull up a calendar; if unchecked, the date will need to be entered manually.
- **Species**: The species that make up this pool.
- **Sex/Condition**: The sex/condition of the arthropods in this pool.
- **# in Pool**: The total number of specimens in this pool. If this pool has specimen from more than one site (denoted in the Other Sites column), the number of specimens from the primary site (Site Code column) will be determined from this value.
- **Comments**: Any accompanying comments.

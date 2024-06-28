---
title: New Site
permalink: /docs/site/
gateway-url: https://gateway.vectorsurv.org/site/ppf/site
youtube-url: https://youtu.be/bzFMqI900KI
---
Sites are essentially bookmarks for trap locations. They will help you quickly record collection events and pool tests without having to locate them on a map or type in coordinates each time.

* **Site Code**: A 6-8 digit numeric identifier for the site. Must be unique to the agency, but not throughout the system.  Each agency can assign codes however they want. Codes that have not yet been assigned for sites in your current agency will be listed in the **Available Ranges** box on the righthand side of the screen. A code of all 0s is given to each agency at their headquarters.
![Available ranges box]({{ site.baseur1}}/assets/images/docs/available-ranges.PNG)
* **Site Name**: Recommended; an easier way to remember the name for the site. Site Code and Site Name will be searchable and autocompleted on the data entry pages so it's helpful to assign this field.
* **Coordinates**: The spatial location for the site. There are 3 ways to assign this, and any one of these methods will overwrite the others. For example, choosing the location on the Map tab will change the coordinates previously entered in the DD tab to match the new position.
  * Type in Latitude/Longitude as Decimal Degrees, Degrees Minutes Seconds, or Degrees Minutes in one of the first three tabs. The point will appear on the Map tab. If the Latitude is in the southern hemisphere or the Longitude is in the western hemisphere, the value must be prefixed by the minus '-' sign.

![Example with coordinates tabs]({{ site.baseurl }}/assets/images/docs/coordinates-ex.PNG)
  * Click on the location on the Map tab. The resulting marker can be moved if necessary.

  ![Example with map tab]({{ site.baseur1 }}/assets/images/docs/coordinates-map-ex.PNG)
  * [Geocode]({{ site.baseur1 }}/docs/tools/spatial-tools) the address either on the Map tab or by filling the address fields below.
* **Coordinate Precision**: Used to specify whether or not a site is marked exactly. Should be kept as *Exact* for most data; this is to specify historical data that might not be as accurate as modern data.
* **Elevation**: The elevation of the site can be calculated via Google Maps once a location is specified.
* **Address**: The address of or nearest intersection to the site.
* **Surroundings**: The surroundings of the site. More than one can be chosen by using the *CTRL/CMD/SHIFT* keys while making selections. If *Other* is specified, a text field will appear to clarify.
* **Population Classification**: Whether the site is *Urban*, *Suburban*, or *Rural*. Can be calculated via census data after a location is specified.
* **Comments**: Any additional notes that should be recorded with this site.

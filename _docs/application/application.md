---
title: New Application
gateway-url: https://gateway.vectorsurv.org/application/ppf/application
youtube-url: https://youtu.be/TZ1xWlObdhc
---
Use this page to keep track of pesticide applications conducted by your agency.

* **Source**: The location of the pesticide application. This can be a point location or over a large polygon. You can add a new source through the [New Source]({{ site.baseurl }}/docs/application/source) page. Start typing in any part of the source code or name and the dropdown will filter the sources to that text.
![Source example]({{ site.baseurl }}/assets/images/docs/source_example.PNG)
Additionally, a one-time source can be added manually using one of the geographical features icons on the map.
![Geographical features]({{ site.baseurl }}/assets/images/docs/geo-features.PNG)
* **Purpose**: The type of pesticide used for this application, or the intended target of the application (adulticide, herbicide, or larvicide).
* **Technician**: The certified individual administering the application. New technicians can be added for your agency through the [technicians configuration page]({{ site.baseurl }}/docs/application/config) page.
* **Equipment**: The equipment used to apply the pesticide. The list of equipment types in the dropdown can be adjusted through the [equipment configuration]({{ site.baseurl}}/docs/application/config) page.
* **Mix**: The pesticide mix used for this application. The list of mixes in the dropdown can be adjusted through the [mix configuration]({{ site.baseurl }}/docs/application/config) page.
* **Quantity**: How much pesticide was used? The first field is used to type in a value and the second field indicates the units.
![Application amount]({{ site.baseurl }}/assets/images/docs/application-amt.PNG)
* **Area**: If the application occurred over a polygon location, how big was the area? Similarly to **Quantity**, the first field is used to type in a value and the second field indicates the units.
* **Start/End Date**: The date on which the application began/ended. Typically, the start and end dates will be the same. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
* **Start/End Time**: The time at which the application began/ended. You can use the dropdown to select the time in 15-minute increments or type in the exact time manually. Time format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
* **Description**: Use this section to describe the application, such as weather conditions, for example.

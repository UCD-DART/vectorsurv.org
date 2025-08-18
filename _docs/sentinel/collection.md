---
title: New Collection
gateway-url: https://gateway.vectorsurv.org/sentinel/ppf/collection
---

Add records of sentinel flock bleeding events.

## Fields

- **Flock Year**: Choose the year, typically the current year unless entering historical data.
- **Flock at Site**: Select the [site]({{ site.baseurl }}/docs/site/) of the flock you will be collecting from using the drop-down arrow.
- **Collection Date**: The date of the bleeding event, typically a future date so printed records have the correct date when going out to make the collection. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
- **Collector**: The name of the person collecting blood samples.
- **Bands**: Once a flock has been selected, each [active]({{ site.baseurl }}/docs/sentinel/flock-manage) Band ID assigned to that flock will appear with a checkbox. Uncheck the boxes for IDs that won't be bled during this collection event. You an also add comments about individual Band IDs.
- **Comments**: Use this section to note anything other users should know about the collection.

The checkboxes below these fields can be used to indicate whether this will be a whole blood submission and whether the collection should be treated as submission-ready. If the whole blood box is checked, all samples from this collection will be treated as whole blood.
![checkboxes]({{ site.baseurl }}/assets/images/docs/sentinel-checkboxes.PNG)

Click the **Add New Collection** button to save the collection.

On the right of the page, there is a box titled **Bulk Collections**. Clicking the text within this box brings up a page to create new collections from one or more sites for one or more dates at the same time. The fields are generally the same as entering a single new collection, except that you have the option to enter multiple sites for the bleeding event for a single collection date or multiple collection dates for a single or multiple sites. Multiple sites can be selected by using the _CTRL/CMD/SHIFT_ keys while selecting values. Each time a collection date is entered, an optional empty box will appear that you can leave empty if not entering more than one date. Note that it will be assumed that all [active]({{ site.baseurl }}/docs/sentinel/flock-manage) Band IDs for each selected flock will be bled.
![Bulk Collections]({{ site.baseurl }}/assets/images/docs/bulk-collections.PNG)

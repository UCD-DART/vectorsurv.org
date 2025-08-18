---
title: Flock Management
gateway-url: https://gateway.vectorsurv.org/sentinel/ppf/band_manage
---

View and edit saved sentinel chicken flocks.

## By Flock

Set the year for which you wish to view active [flocks]({{ site.baseurl }}/docs/sentinel/new-flock) using the dropdown arrow and clicking the **Change Year** button to change years. The resulting table shows all active flocks for that year. The **# of Bands** column shows how many bands are Active/Total in that flock (this status can be managed in the **By Band** table below). The **# of Bleeds** column shows the number of bleeding events that have occurred at that flock while the **# of Bands Bled** column notes how many individual bands were recorded over the course of those bleeding events. The **# of Positives** column shows how many bands were Presumptive/Confirmed for antibodies. The **Active?** column is a checkbox to untick if that flock is no longer active. Finally, the **Actions** column allows you to edit that flock's information. Clicking the edit link will bring you to a page where you can edit, add, or assign bands to that flock. Click the **Update Flock** button to save any changes or the **Back to Flock Management** button to leave the page. Beneath the table, you can navigate between pages using the arrows or by typing in the page number. You can also change how many collections to display on a single page using the drop down option.
![Arrows under table]({{ site.baseurl }}/assets/images/docs/table-search.PNG)

## By Band

This table displays every **Band ID** in use during the selected year and each ID's associated **[Site]({{ site.baseurl }}/docs/site/)**. The **# of Bleeds** column shows how many times that individual band was bled during the selected year. The **Positive?** column shows whether that Band ID was Confirmed positive (red) and/or Presumptive positive (orange) for antibodies.
![sentinel results]({{ site.baseurl}}/assets/images/docs/sentinel-pos.PNG)
The **Active?** column is a checkbox to untick if that band ID is no longer active. The **Actions** column allows you to assign Local IDs if you are using different band numbers than the official band numbers. Click the **Save** button to save the associated Local ID or the **Close** button if you don't wish to make changes. Finally, any bands without an associated flock can be deleted. Beneath the table, you have the same navigation options to search within the table.
![local IDs]({{ site.baseurl }}/assets/images/docs/local-id.PNG)

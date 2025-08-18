---
title: Test Result Management
gateway-url: https://gateway.vectorsurv.org/sentinel/ppf/test_manage
---

View and edit saved sentinel chicken test results.

Select the month and year for which you wish to view results by choosing the appropriate values using the drop-down arrows. Click the **Change Month/Year** button to make the change.

You can view the results either by [Collection]({{ site.baseurl }}/docs/sentinel/collection), by Date of Collection, or by [Flock]({{ site.baseurl }}/docs/sentinel/new-flock). Any of these tables can be minimized and/or maximized by clicking on the respective title next to the arrow.

### By Collection

This table shows all test results by [Collection ID]({{ site.baseurl }}/docs/sentinel/collection) for the selected time frame. It displays information about the collection, including **Collection Date**, **# of Bands**, and **# of Positives** (format: Presumptive/Confirmed). Clicking the _View_ link under the **Actions** column takes you to the details for that collection's results if results for that collection have been submitted. Here, you can _edit_ or _delete_ that result. Editing will pull up a pop-up box with the same fields as the new test result page, which you can then save. Do this if you need to change the **Status** of the test result from Pending to Positive or Negative, for example.

### By Date of Collection

This table shows all test results by **Collection Date** for the selected time frame. It shows how many collections were made on that date and the total number of samples that were tested from those collections. Clicking the _View_ link under the **Actions** column pulls up the detailed results for each [Band ID]({{ site.baseurl }}/docs/sentinel/new-flock) that was sampled on that date, which can be edited and/or deleted in a manner similar to above.

### By Flock

This table shows all test results by [Flock ID]({{ site.baseurl }}/docs/sentinel/new-flock) for the selected time frame. **# of Bands** shows how many Active/Total bands are in that flock, while the **# of Collections** and **# of Samples** show the number of [collections]({{ site.baseurl }}/docs/sentinel/collection) and the total number of samples from those collections from each flock. The **# of Positive** shows the number of Presumptive/Confirmed positive samples in that flock. **Active?** indicates whether that flock is currently active. Clicking the _View_ link under the **Actions** column takes you to the detailed results for each sample from every Band ID that can be edited and/or deleted as above.

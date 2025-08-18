---
title: New Results
gateway-url: https://gateway.vectorsurv.org/sentinel/ppf/test_add
---

Use this page to enter sentinel chicken test results.

### Fields

- **Year**: The active year of the [flock]({{ site.baseurl }}/docs/sentinel/new-flock) you are testing.
- **Band**: The [Band ID]({{ site.baseurl }}/docs/sentinel/new-flock) this sample was collected from. Clicking in the box will pull up a drop-down list of available IDs. You will not be able to enter a Band ID that was not active in the selected year.
- **Collection Date**: The date of the bleeding event.
- **Test Date**: The date of the test. The test date and collection date fields can be entered manually or using the calendar feature that appears when you click in the field.
- **Method**: The type of test used.
- **Target**: The pathogen target for this test.
- **Value**: Here you can add the result from the test, or the value can be added later through the editing feature if you don’t yet have results.
- **Status**: The pathogen status for this Band ID following test results. If results are not yet known, select _Pending_.
- **Comments**: Click the ellipses to add any relevants about this test.

You can insert new rows by clicking on the row number.
![insert new row]({{ site.baseurl }}/assets/images/docs/insert-row.png)

There is a box on the right-hand side of the screen to load samples from specific [collections]({{ site.baseurl }}/docs/sentinel/collection) into the New Results table if all the corresponding collections were tested on the same date. Clicking the link in the box will pull up a pop-up window requiring you to select the Year, Submission ID, and Test Date. You can choose to fill in the fields for Method, Target, and Status if all the samples for that Collection ID have the same values. Leaving these fields blank will allow you to edit them individually on the table before adding the new test results. Close the window once the samples have been loaded into the table. Note that loading samples in this way will delete any previously entered data.

Note that if a sample is tested for multiple targets, you will need to provide a result for each target.

When finished, click the **Add Test Results** button to save the changes.

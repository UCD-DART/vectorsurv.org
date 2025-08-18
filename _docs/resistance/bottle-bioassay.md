---
title: New Bottle Bioassay
gateway-url: https://gateway.vectorsurv.org/resistance/ppf/bottle
---

Import new bottle biassay results using this page.

- **Name**: Name this bottle biassay so it can be searched for later under Manage Bottle Bioassays
- **Date**: The date this bottle bioassay was performed. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
- **Material**: Use the dropdown arrow to choose the material used for this bottle bioassay.
- **Diagnostic Dose**: This is the dose of your chosen material that kills 100% of susceptible mosquitoes within a pre-determined time period.
- **Lot #**: The lot # for this batch of material.
- **Synergist**: If a synergist was used with this material, use the dropdown arrow to choose which synergist was uesd.
- **Synergist Dose**: The dose of synergist used.
- **Synergist Lot #**: The log # for this batch of synergist.
- **Control Mortality %**: The percent of mosquitoes that died in the control (no pesticide) bottle. Should be a value between 0 and 100.
- **Tested By**: The name of the person performing the bottle bioassay.
- **Description**: A description of the bottle bioassay performed or any notes regarding this test.
- **Test Defaults**: There are three default settings for new bottle bioassays that are modifiable. **Mosquito Count** is the starting count in each bottle. Individual bottles can be changed later. **Default Time Span** is the time period between each mortality count. **Default Number of Timing Events** is the number of mortality counts that will be entered.
  ![Test Defaults]({{ site.baseurl }}/assets/images/docs/test-defaults.PNG)

When finished entering the fields above, click on the _Add test species_ link to add mortality data. ![add species link]({{ site.baseurl }}/assets/images/docs/add-species.PNG)

You are required to choose the species that was tested by typing in the species name or using the dropdown arrow to choose the species as well as whether the tested mosquitoes were from a colony or field-collected. If these were colony mosquitoes, enter the colony name and a brief description of this colony. If they were field-collected, give the generation, collection date, and a brief description of the collection, and indicate on the map where the collection came from by typing in coordinates or using the marker tool.

The table below is automatically generated based on the **Test Defaults** settings. Enter either the number _Alive_ or _Dead_ for each time point. The other field will autofill based on the starting count. You can add rows by clicking on **Add Additional Time Series** or delete rows by clicking on the bin icon next to the time point. You can also edit time points by clicking in the text box. You can also add columns by clicking on **Add Replicate** or delete columns by clicking on the bin icon next to the replicate number.
![Bottle Bioassay]({{ site.baseurl }}/assets/images/docs/bioassay.PNG)

Click the **Add Bottle Bioassay** button to save the test.

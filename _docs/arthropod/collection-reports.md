---
title: Collection Reports
gateway-url: https://gateway.vectorsurv.org/arthro/ppf/report
---

Collection reports automatically generate Arthropod Collection and/or Arthropod Occurrence Reports.

- **Agency**: Choose the agency for which you wish to generate the report(s). You can select multiple agencies by using the _CTRL/CMD/SHIFT_ keys while selecting values. If more than one agency or the **All Available Agencies** option is selected, a report is generated for each agency.
- **Disease Week**: Use the drop-down arrows to select the epi-week and year for which to generate the report. This autofills the **Date Range** field.
- **Date Range**: This field is autofilled from the **Disease Week** selection. You can also enter dates manually into the boxes for date ranges longer or shorter than one week. Date format is based on the settings under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
  ![Date Range]({{ site.baseurl }}/assets/images/docs/disease-week.PNG)
- **Trap Type**: Check the boxes next to the trap types to generate reports for. If more than one trap type is selected, a report is generated for each trap type.
- **Report**: Choose the type of report to generate from **Arthropod Collection Report** and **Arthropod Occurrence Report** by checking the box next to the report type.
  - **Arthropod Collection Report**: If selected, you will be able to determine the **Report Format**. The default for the ACR is a Microsoft Excel spreadsheet, but you can change the format through the drop-down menu. The settings for the type of file to generate can be managed under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences). There is a checkbox that is checked by default for the ACR to use the site/species sort order from the trap type's default [worksheet]({{ site.baseurl }}/docs/arthropod/worksheets), which can be done by selecting a trap type on a specific worksheet under **Worksheet Management**. If checked, the default worksheet for a trap type's ordering of sites and species will be used, otherwise the order of sites and species will be alphabetic. Finally, you can filter the collections based on the number of nights the trap(s) ran. Typically, reports are based on All Available Trap Nights.
    ![ACR]({{ site.baseurl }}/assets/images/docs/acr.PNG)
  - **Arthropod Occurrence Report**: If selected, you will be able to determine the **Report Format**. The default for the AOR is a Microsoft Word document, but you can change the format through the drop-down menu. The settings for the type of file to generate can be managed under [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences). There are two checkbox options for producting the AOR. First is a box that is checked by default to treat each agency individually. If checked, one occurrence report will be generated for each selected agency, otherwise all selected agencies are grouped together. The second checkbox that is unchecked by default gives the option to output report(s) as a single spreadsheet instead of a text document.
    ![AOR]({{ site.baseurl }}/assets/images/docs/aor.PNG)

Clicking the **Generate Report(s)** button at the bottom of the page will create the selected report(s). The ACR is a summary of all arthropod species collected at each selected agency in each selected trap type during the specified time period. The AOR summarizes major vector species and genera based on the total number of females collected per trap-night in Urban, Suburban, and Rural settings.

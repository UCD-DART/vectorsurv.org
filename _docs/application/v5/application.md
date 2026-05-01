---
title: New Application
gateway-url: https://gateway.vectorsurv.org/v5/application/application
v5: true
---

## Pesticide Application Tracking

Use this page to record and manage pesticide applications conducted by your agency.

- **Source**: The location of the pesticide application (point or polygon).
  - **Existing Source**: Start typing a name or code in the input field to filter the dropdown list. New permanent sources can be added via the [New Source]({{ site.baseurl }}/docs/application/v5/source) page.
  - **One-time Source**: Use the drawing tools on the left side of the map to manually define a location. Once drawn, editing tools will appear to allow for precise adjustments.
  - **Recenter**: Click the blue **Recenter** icon ![Recenter Button]({{ site.baseurl }}/assets/images/docs/recenter-btn.png) in the lower right-hand corner of the map to pan the view to the current source.

  ![Source selection example]({{ site.baseurl }}/assets/images/docs/application-v5/source_input.PNG)

- **Purpose**: The type of pesticide used or the intended target of the application (e.g., adulticide, herbicide, or larvicide).
- **Technician**: The individual administering the application. New technicians can be managed through the [Technicians Configuration]({{ site.baseurl }}/docs/application/v5/config/config) page.
- **Equipment**: The equipment used for the application. The available options in this dropdown can be adjusted through the [Equipment Configuration]({{ site.baseurl }}/docs/application/v5/config/config) page.
- **Mix**: The pesticide mix used. The list of available mixes can be adjusted through the [Mix Configuration]({{ site.baseurl }}/docs/application/v5/config/config) page.
- **Quantity**: The total amount of pesticide applied. Enter the numerical value in the first field and select the appropriate units in the second field.

  ![Application quantity input]({{ site.baseurl }}/assets/images/docs/application-v5/quantity_input.PNG)

- **Area**: The size of the treated area (applicable for polygon locations). Like the **Quantity** field, enter the numerical value in the first field and the units in the second.
- **Start/End Date**: The date on which the application began and ended. Typically, these dates will be the same. The date format is determined by your [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
- **Start/End Time**: The time at which the application began and ended. You can select a time in 15-minute increments from the dropdown or type the exact time manually. The time format is determined by your [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
- **Description**: Use this field to provide additional context for the application, such as specific weather conditions or site observations.

---

> **Quick Tip:** If you need to review this documentation just click the help icon located in the title bar. ![Help Icon]({{ site.baseurl }}/assets/images/docs/help-icon.PNG)

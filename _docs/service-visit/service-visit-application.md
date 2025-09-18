---
title: Associated Application
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/servicevisit/visit
---

After creating a Service Visit record a new Application card will appear below the Service Visit form. Users may create new Application records here or link already existing Applications. Applications will appear on PUR reports and can be viewed or edited in the Application module as well as here.

![Associated Collections Card](/assets/images/docs/application-card-service-visit-module.png)

**Table**

Any associated applications will be displayed in the table here. Users can sort the table by clicking on the appropriate column header. Clicking on the "pencil" icon will allow the user to edit the associated application. The "link-slash" icon will unlink the Application record from the Service Visit.

**Linking Applications**

Clicking the **Link Application** button will open up a panel for associating existing application records
![Address input](/assets/images/docs/application-modal.PNG)

- The map will show all Applications within seven days of the Service Visit record.
- Clicking on a "link" icon in the Available Applications table will associate the record with the current Service Visit.
- Clicking on the "link-slash" icon in the Linked applications table will unlink the Application record from the Service Visit.

**Add Applications**

Clicking the **Add Application** button will open up a panel for creating new associated Application records.

**Create Application Form**

![Address input](/assets/images/docs/application_form_service_visit_module.png)

**Fields**

- **Source**: The location of the pesticide application. This can be a point location or a polygon. You can add a new source through the New Source page. Start typing any part of the source code or name and the dropdown will filter the sources to that text. A One Time Source can also be created specifically for the current application by using the drawing tools on the left.

- **Purpose**: The type of pesticide used for this application, or the intended target of the application (adulticide, herbicide, or larvicide).

- **Technician**: The certified individual administering the application. New technicians can be added for your agency through the technicians configuration page.

- **Equipment**: The equipment used to apply the pesticide. The list of equipment types in the dropdown can be adjusted through the equipment configuration page.

- **Mix**: The pesticide mix used for this application. The list of mixes in the dropdown can be adjusted through the mix configuration page.

- **Quantity**: How much pesticide was used? The first field is used to type in a value and the second field indicates the units.

- **Area**: If the application occurred in a polygon location, how big was the area? Similarly to Quantity, the first field is used to type in a value and the second field indicates the units.

- **Start/End Date**: The date on which the application began/ended. Typically, the start and end dates will be the same. Date format is based on the settings under Account Preferences.

- **Start/End Time**: The time at which the application began/ended. You can use the dropdown to select the time in 15-minute increments or type in the exact time manually. Time format is based on the settings under Account Preferences.

- **Description**: Use this section to describe the application, such as weather conditions.

After filling out the form you can click the **Save** button to submit the data. You can also **Clear** the fields or **Cancel** and close the form at any time.

---
title: Associated Inspection
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/servicevisit/visit
---

After creating a Service Visit record a new Collection/Inspection card will appear below the Service Visit form. Users will have the ability to create or link associated Inspection/Collection records.

![Inspection Card](/assets/images/docs/inspection-card-service-visit-module.png)

**Table**

Any associated Inspections will be displayed in the table here. Users can sort the table by clicking on the appropriate column header. Clicking on a "pencil" icon will navigate the user to the appropriate Collection Update form where they can make corrections as needed . The "link-slash" icon will unlink the Inspection/collection record from the Service Visit.

**Linking Inspections**

Clicking the **Link Collection** button will open up a panel for associating existing collection records

![Address input](/assets/images/docs/Inspection_link_form_service_visit_module.png)

- The map will show all Collections within seven days of the Service Visit record.
- Clicking on a "link" icon in the Available Collections table will associate the record with the current Service Visit.
- Clicking on the "link-slash" icon in the Linked Collections table will unlink the Application record from the Service Visit.

**Add Inspection/Collection**

Clicking the **Add Inspection** button will open up a panel for creating new associated Inspection records. These are are Arthro Collection records with a trap type of either "Household Inspection (counts)" or "Household Inspection (presence/absence)".

**Create Inspection Form**

![Address input](/assets/images/docs/inspection_form_service_visit_module.png)

**Fields**

- **Trap**: The type of inspection made at the Service Visit site. Choices include "Household Inspection (counts)" or "Household Inspection (presence/absence)". If a choice is missing please review your agency trap configuration [Trap Types Configuration]({{ site.baseurl }}/docs/arthropod/trap-types/).

**Site**
The user will be able to place the inspection at either an existing site or create a new site here in the form by using the "Create New Site" toggle.

- **Site Code**: Start typing in any part of the site code or name and the dropdown will filter the sites to that text. Selecting a site code from the dropdown select will place a marker on the map. If creating a new site just enter the desired numeric site code. It must be unique within your agency.

- **Site Name**: This field is only available when creating a new site. It is intended to be an easily memorable moniker for the site. It does not need to be unique.

- **Latitude and Longitude**: When choosing an existing site these fields will automatically be populated. If creating a new site coordinates may be entered manually or by clicking on the map. Doing so will create a marker at the desired location.

- **Coordinate Precision**: Used to specify the level of certainty in the latitude & longitude coordinates. The default is "Exact".

**Abundance**
Add the abundance counts for any species found during the inspection. Fill out the form and click "Add To Table" as many times as needed.

- **Identified By**: The person who identified the arthropods from this inspection.

- **Species**: The species that make up this abundance. Start typing to filter the list. The list of species in the dropdown can be adjusted through the Available Species settings on the arthropod configuration page.

- **Sex/Condition**: The sex/condition/life stage of the abundance. Start typing to filter the list.

- **Count**: Number of specimens in the abundance. Minimum of 1 for counted Inspections. "Present" designation is used when the Inpsection type is "presence/absence".

- **Comments**: Add any desired comments.

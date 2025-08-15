---
title: New Collection
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/mosquito/collection/collection
youtube-url: https://youtu.be/qeGHkn215jQ
---

Collections are the records of arthropod population data through the
placement of traps.

## Date

**Fields**

Date format is based on the settings under [Account
Preferences]({{ site.baseurl }}/docs/settings/account-preferences).

There are two ways to input the collection date. You can choose your
preferred method by clicking on the toggle button that says "Input by
start/end dates".

Toggle button off:

- Enter a single collection date and number of nights the trap was in
  the field. The collection date is the date the trap was picked up.
  The start date for the trap will be calculated by subtracting the
  trap nights from the provided collection date. A trap placed and
  collected on the next day would be 1 trap night. Because the minimum
  is 1 night, if a trap was placed and collected on the same day,
  enter 1.

Toggle button on:

- Enter collection start and end dates. The trap nights field will be
  automatically calculated based on the provided dates and cannot be
  edited by the user.

**Fields**

- **Timezone:** Displays the current timezone. Click on it to open a
  modal where you can select a custom timezone.

- **Collection Date** or **Collection End Date**: The date the trap
  was picked up / last day of the collection. You can type a date
  value in the format set under [Account
  Preferences]({{ site.baseurl }}/docs/settings/account-preferences)
  or pick a date using the datepicker UI. The \# column on the left
  with the gray boxes represent disease weeks. These are for
  reference-only and cannot be selected.

- **Collection Start Date:** The date the trap was set up / the
  collection was started. You can type a date value in the format set
  under [Account
  Preferences]({{ site.baseurl }}/docs/settings/account-preferences)
  or pick a date using the datepicker UI. The \# column on the left
  with the gray boxes represent disease weeks. These are for
  reference-only and cannot be selected.

- **Trap Nights**: Number of nights the trap was in the field. Minimum
  is 1 night. If a trap was placed and collected on the same day,
  enter 1.

## Site

The [site]({{ site.baseurl }}/docs/site/) where a trap was placed. A
collection date needs to be selected before you can choose a trap site.

- **Site Code**: Start typing in any part of the site code or name and
  the dropdown will filter the sites to that text. Selecting a site
  code from the dropdown select will place a blue marker on the map.
  You can also select a site using the 'Show Existing Sites' toggle in
  the Map section.

- **Map**: Clicking on the "Map" heading will expand the map panel to
  give a view of the site area. Once a site is selected, the trap can
  be dragged to a new location up to 400m away indicated by the
  circle.

  - **Zero Site Code**: Collections using the Zero Code will have no
    buffer zone and can be placed anywhere on the map. You can read
    more about Zero Site Codes in the [Site
    documentation.]({{ site.baseurl }}/docs/site/v5/new-site)

  - **Latitude and Longitude:** These fields will be automatically
    populated once a site is selected, and they can be adjusted with
    the same 400m limitation mentioned above.

  - The user can make the map zoom in and out using the "+/-"
    buttons in the upper left hand corner, or by scrolling while
    hovering over the map.

  - The "Show Existing sites" toggle will add gray markers for other
    existing sites to the map You can click on a site to see the
    site details and select 'Set As Site' to select it as the
    collection's trap site. Clicking the blue "recenter" icon in the
    lower right-hand corner of the map will cause the map view to
    pan over to the current site marker.

![Site Map Card](/assets/images/docs/site-map.png)

- **Latitude:** The latitude value. Must be between -90 & 90 degrees.

- **Longitude:** The longitude value. Must be between -180 & 180
  degrees.

- **Precision:** Used to specify the level of certainty in the site
  coordinate. In most cases, this field should be kept as Exact. For
  historical data, instances where the exact location is uncertain or
  in instances where the exact location need to be obscured due to
  human case privacy concerns, the user may choose the most accurate
  option from the list.

## Trap Details

**Fields**

- **Trap**: The type of trap placed in the field. The list of traps in
  the dropdown can be adjusted through the Trap Types settings on the
  [arthropod configuration
  page]({{ site.baseurl }}/docs/arthropod/trap-types/).

- **Lure(s)**: The types of lure(s) used with the trap if any.
  *Unspecified* and *None* can only be selected individually.

- **\# of Traps**: The number of unique traps in operation at one
  site.

- **Identified By**: The person who identified the arthropods in this
  trap.

- **Trap had problems?**: If checked, the trap used for this
  collection is considered to have experienced any mechanical
  failures, i.e. fan broke, dead battery, etc. Leave unchecked if the
  trap did not experience a problem during the trapping period.

## Comment

Use this section to note anything other users should know about the
collection, including the reason(s) for trap failure, for example.

## Species Count {#species-count}

Use this section to enter arthropods found in the trap.

**Ticks:** Use the [tick
module]({{ site.baseurl }}/docs/tick/tick-menu/) if entering a tick
collection. Historical data where a tick species was entered under an
arthropod collection may be viewed here but not edited. A link to the
legacy form is provided in case you need to edit the data.

### Input Methods:

You will see a single mobile-friendly form if your screen size is smaller than 768px. If your screen size is larger than 768px, there you will see two input methods: A tabular input similar to the legacy form where you can update multiple abundances in one go and the mobile-friendly form where you can input one abundance at a time. The input style will remember the last selection you made (e.g.: If you selected Form Input, it will always load on Form Input until you select Tabular Input, then it will always load the Tabular Input first.)

Note: Edits made using either style of input are not saved until the Save Collection or Update Collection button has been clicked.

#### Tabular Input

![Tabular Input](/assets/images/docs/new_collection_tabular.png)

- To enter an abundance first select the species that make up this abundance. Start typing to filter the list. Each row must have a unique species not already entered for this collection. The list of species in the dropdown can be adjusted through the Available Species settings on the [arthropod configuration page]({{ site.baseurl }}/docs/arthropod/trap-types/).
- When you select a species a new unpopulated row will automatically appear. This is for convenience so the user does not have to manually create each new row. This will not create a new empty abundance.
- After a species is selected, you can input counts for each sex/stage/condition column. ‘Σ F’ represents the total number of females for the row’s species across F-Mixed, F-Unfed, F-Bloodfed and F-Gravid. Each row must have at least one count. It is not necessary to mark 0 counts as that is assumed when left blank or absent from the form.
  - You can enter either F-Mixed OR any combination of F-Unfed, F-Bloodfed and F-Gravid. For example, if you input a count for F-Bloodfed, the F-Mixed input will become disabled. If you input a count for F-Mixed, F-Unfed, F-Bloodfed and F-Gravid will all be disabled.
- The bottom row represents totals for each sex/stage/condition across species.
- **Action Buttons:**
  ![Gray X icon](/assets/images/docs/action-button-remove.png) Remove the selected row.
- **Keyboard Shortcuts:**
  While focused on a cell, hold Ctrl + Alt + C (Windows) or Ctrl + ⌘ + C (Mac) to copy the abundance to the Pool form below. If entering abundance for a presence-type trap, you can focus on a cell without checking/unchecking the input by clicking just to the left of the checkbox and pressing tab.

#### Form Input

![Species Form Input](/assets/images/docs/new_collection_species_form.png)

- **Fields**

  - **Species**: The species that make up this abundance. Start typing
    to filter the list. The list of species in the dropdown can be
    adjusted through the Available Species settings on the [arthropod
    configuration
    page]({{ site.baseurl }}/docs/arthropod/trap-types/).

  - **Sex/Condition**: The sex/condition/life stage of the abundance.
    Start typing to filter the list.

  - **Count:** Number of specimens in the abundance. Minimum of 1.

### Abundance Table:

- **Action buttons**:

  ![Copy icon](/assets/images/docs/action-button-copy.png): Copy the selected abundance to the pool form. The species, sex and count of the selected abundance will be copied to the pool form.

  ![Pencil icon](/assets/images/docs/action-button-edit.png): Edit the selected abundance. The
  abundance information will populate in the form and will no longer be
  viewable in the table. (The data is only moved locally -- if you do not
  finish editing the form or there are technical issues the abundance data
  will still be saved on the collection.)

  ![Gray X icon](/assets/images/docs/action-button-remove.png) Remove the selected abundance from the table. (The data is only removed locally -- you must save/update the collection to persist this change.)

  ![Go to legacy site](/assets/images/docs/action-button-legacy-link.png): Return to the legacy form to edit a
  tick abundance.

- **Totals**:

  - Total females: Total number of female specimen across all abundances
    in the table.

  - Total: Total number of specimens of any sex across all abundances in
    the table.

## Pool

Optionally, a pool for arbovirus testing can be entered or linked
through the collection page. This links the pool to the collection that
the pool originated from.

**Generate Pool(s):**

Use this form to enter new pool(s) linked to this collection or edit
existing pools linked to this collection.

**Fields**

- **Pool Number**: A numeric identifier for the pool. Pool numbers
  have to be unique per agency per year. Normally you would start at 1
  and increment throughout the year but the exact numbering scheme is
  up to you. Available numbers for your agency are shown in the aside
  menu on the righthand side of the page. Open the orange Pool \#
  Availability card. You can open and close the menu using the small
  arrow tab on the far-right edge of the page.

![Collection Form Aside Menu](/assets/images/docs/aside-collection-form.png)

- **Method:** The list of traps in the dropdown can be adjusted
  through the Trap Types settings on the [arthropod configuration
  page]({{ site.baseurl }}/docs/arthropod/trap-types/).

- **Species:** The species that make up this pool. Start typing to
  filter the list. The list of species in the dropdown can be adjusted
  through the Available Species settings on the [arthropod
  configuration
  page]({{ site.baseurl }}/docs/arthropod/trap-types/).

- **Sex/Condition:** The sex/condition/life stage of the arthropods in
  this pool.

- **Comments:** Any accompanying comments.

- **Generating New Pools:** These fields only appear when generating new pools. Pools to be generated will appear in the New Pools table. They are not permanently saved until the Save/Update Collection button has been clicked.

  - **Total Count:** The total number of specimens in this
    pool/across all pools (if generating batches of more than one pool). Minimum of 1. After selecting a species and sex/condition combination, the field will autopopulate with counts from abundances provided in the Species Card, if available.

  - **Max Pool Size:** The maximum size of each pool to be generated. For example, if generating pools for 125 specimens total with a max pool size of 50, there will be two pools of 50 to make 100 and one leftover pool of 25 to meet the total count. Minimum of 1.

  - **\# of Pools:** View-only field. The number of pools to be generated.

  - **Add New Pool(s):** You must first click this button to generate new temporary pools you can view and edit. Once the temporary pools are generated, you must click Save/Update Collection to save them permanently, after which they will appear in the Linked Pools table.

- **Updating a single pool:**

  - **Count:** The total number of specimens in this pool. Minimum of 1.
  <!-- invisible character to create shortcut without making it a header -->

###### ‎ {#secondary-sites}

- **Secondary Sites:**
  If the pool contains specimens from more than one trap, up to two secondary sites can be added. To indicate where the additional specimens were collected, enter the site code for their collection location. It is also recommended to enter a count of the specimens included so that VectorSurv can validate the pool sample count.

  Note that calculations in VectorSurv are based on the specified location of the pool, not the location of additional specimens from secondary sites.

**New Pools**
A table of temporary pools that will be saved when the Save/Update Collection button is clicked.

- Action buttons:

  ![Pencil icon](/assets/images/docs/action-button-edit.png): Edit the selected pool. The pool
  information will populate in the form and will no longer be viewable in
  the table. (The data is only moved temporarily -- clearing the pool form will return the pool to the New Pools table)

  ![Gray X icon](/assets/images/docs/action-button-remove.png) Remove the selected row.

  **Clear New Pools:** Removes all rows from the New Pools table.

**Link Existing Pools:**

A table of pools eligible to be linked to the current collection. You
can click on the link button to the right of a pool to link a pool to
the collection. Linking a pool will overwrite the **collection date**,
**site, lures** and **trap** values with those of the collection. It
will also remove any **secondary sites** associated with the pool.

**Linked Pools Table:**

A list of all pools linked to the current collection. If a pool has a
positive test result, the Positive? column will show an abbreviation in
red of what it was positive for.

- Action buttons:

  ![Pencil icon](/assets/images/docs/action-button-edit.png): Edit the selected pool. The pool
  information will populate in the form and will no longer be viewable in
  the table. (The data is only moved locally -- if you do not finish
  editing the form or there are technical issues, the abundance data will
  still be saved on the collection.)

  ![Unlink icon](/assets/images/docs/action-button-unlink.png): Unlink the selected pool. This will
  remove the link between the pool and the collection.

  ![Red trash can icon](/assets/images/docs/action-button-delete.png): Delete the selected pool.

- Totals:

  - Total Count: Total number of specimen across all pools in the table.

  - Total Pools: Total number of pools linked to the collection.

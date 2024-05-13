---
title: Walkthroughs
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/site/site
---

Creating and editing site revisions can be complicated. Below are some
walkthroughs of common tasks.

- [Create a new site](#new-site)
- [Create a new site with a specific date interval](#new-site-interval)
- [Edit an existing site's optional values](#edit-optional)
- [Edit an existing site's date values](#edit-date)
- [Edit an existing site's coordinates](#edit-coordinates)
- [Create a new site revision](#new-revision)
- [Edit the date boundary between two date-adjacent sites](#edit-date-boundary)
- [Merge two date-adjacent sites](#merge-sites)

<div id="new-site"></div>
<br />

### **Create a new site.** {#new-site}

**Scenario**: You are creating a new site in the VectorSurv system for
your agency to use with the following characteristics\...

- The **site code** is **unique** (i.e., it has never been used by
  your agency).
- The site location is **currently** being used to trap specimens.

- You want to be able to add **historical** records (e.g., pools and
  collections) utilizing this site at **any point in time**.

**Steps:**

1.  Navigate to the "Create New Site" page (e.g. Sites -\New Sites).

2.  Leave the "Active Date" and "Deactive Date" fields blank.

3.  Enter a "Site Code" that is unique to your agency throughout
    history. Note: The code could be used by another agency (e.g., both
    agency #1 and agency #2 could have a site with code 1000001).

4.  Specify the site location by entering the Latitude and Longitude, by
    entering the address, or by clicking the location on the map.

5.  (specify any required fields here)

6.  Add values for optional fields (e.g., Site Name, Address,
    Surroundings, Comments) if desired.

7.  Click the "Save Site" button.

<div id="new-site-interval"></div>

**Results**: The site has been created and can be referenced when
generating various records throughout the VectorSurv system. You can
see a list of existing sites for your agency on the "Manage Sites"
page.

---

### **Create a new site with a specific date interval.**

**Scenario**: You want to create a new site in the VectorSurv system for
your agency to use with historical collection and/or pool records. You
want the site to have the following characteristics\...

- You want to record the date the site was decommissioned. The site
  location is **NOT** currently being used to trap specimens and your
  agency doesn't plan to use this location in the future.

- You want to record the date when the site location was first used to
  collect specimens.

- The **site code** is **unique** in this interval (i.e., the code was
  not used by your agency at any other location during the desired
  time period).

**Steps:**

1.  Navigate to the "Create New Site" page (e.g. Sites -\New Site).

2.  Enter the appropriate values in the "Active Date" and "Deactive
    Date" fields.

3.  Add a "Site Code" that is unique to your agency during this
    interval.

4.  Fill in the other required fields (i.e., Latitude and Longitude).

5.  Add values for optional fields (e.g., Site Name, Address,
    Surroundings, Comments) if desired.

6.  Click the "Save Site" button.

<div id="edit-optional"></div>

**Results**: The site has been created and can be referenced when
generating various records with collection dates that fall within the
time interval between the site's Active and Deactive dates. You can
see a list of existing sites, and their relevant dates, on the "Manage
Sites" page.

---

### **Edit an existing site's optional values.**

**Scenario**: Your agency has a site record in our system, and you wish
to update the value of some optional fields (e.g., Address or Comments).

**Steps:**

1.  Navigate to the "Manage Sites" page (e.g. Sites -\Manage Sites).

2.  Find the desired site in the site table and click on the "Edit"
    button (i.e., The Pencil icon). This will bring you to the "Edit
    Site" form.

3.  Edit the values for optional fields as desired.

4.  Click the "Update Site" button.

<div id="edit-date"></div>

**Results**: The site values will be updated. The newly edited values
will apply throughout the site's history.

---

### **Edit an existing site's date values.**

**Scenario**: Your agency has a site record in our system, and you wish
to change the "Active Date" and/or "Deactive Date" value(s).

**Steps:**

1.  Navigate to the "Manage Sites" page (e.g. Sites -\Manage Sites).

2.  Find the desired site in the site table and click on the "Edit"
    button (i.e., The Pencil icon). This will bring you to the "Edit
    Site" form.

3.  In the "Date Range" section you may edit only one date value at a
    time. For validation reasons, editing both date fields requires two
    submissions. Once a date value has been edited the other date field
    will be disabled until the form is submitted (i.e., If you edit the
    "Active Date" the "Deactive Date" field will be temporarily
    disabled).

4.  Click the "Update" button in line with the edited field.

5.  After a successful submission the date has been edited. If you wish
    to edit the other date field, you may do so now.

<div id="edit-coordinates"></div>

**Results**: The site date value(s) will be updated. Records can be
associated with the new date range. Note: If the new site revision
dates overlap with other existing revisions you will see a warning
message.

---

### **Edit an existing site's coordinates.**

**Scenario**: The coordinates for one of your agency's sites were
entered incorrectly. You want to edit the coordinates and have the new
location apply to all associated records throughout the site revision's
history.

**Steps:**

1.  Navigate to the "Manage Sites" page (e.g. Sites -\Manage Sites).

2.  Find the desired site in the site table and click on the "Edit"
    button (i.e., The Pencil icon). This will bring you to the "Edit
    Site" form.

3.  Edit the location by specifying the latitude and longitude or by
    selecting the location on the map.

4.  Click the "Update Site" button.

<div id="new-revision"></div>

**Results**: The site's coordinates will be updated. The site's
"buffer zone" will also be updated. All associated records will have
their locations changed to the new site coordinates. (**Note**: This
**includes** any records that may have been "offset" during their
creation).

---

### **Create a new site revision.**

**Scenario**: Your agency will no longer be using a particular location
as a trap site. You want to reuse that site code and have it associated
with another location for all future collection dates.

**Steps:**

1.  Navigate to the "Manage Sites" page (e.g. Sites -\Manage Sites).

2.  Find the site you wish to deactivate in the site table and click on
    the "Edit" button (i.e., The Pencil icon). This will bring you to
    the "Edit Site" form.

3.  Edit the deactive date value as needed.

4.  Click the "Update" button in line with the "Deactivate Date" field.
    After a successful update the site is no longer active after the
    deactive date.

5.  Scroll down to the bottom of the page and expand the "Revisions"
    card if necessary.

6.  Click the "Create New Revision" button.

7.  You should now be viewing the "Create New Site Revision" form.

8.  Enter the appropriate values in the "Active Date" and "Deactive
    Date" fields. Leave the "Deactive Date" field blank if the site is
    currently active. This date range cannot overlap any existing site
    revisions for this site code.

9.  The "Site Code" field will have the appropriate value already filled
    in.

10. Fill in the other required fields (i.e., Site Name, Latitude, and
    Longitude).

11. Add values for optional fields (e.g., Address, Surroundings,
    Comments) if desired.

12. Click the "Save Site" button.

<div id="edit-date-boundary"></div>

**Results**: A new site revision for this site code has been created.
You can associate records whose collection dates fall within this
revision's active/deactive date range.

---

### **Edit the date boundary between two date-adjacent sites.**

**Scenario**: Two site revisions have been created for your agency with
the same site code. The "Active Date" of the more recent site is
incorrect and needs to be edited. The resulting edit will cause this
revision's date range to overlap the previous site revision's date
range. This is intentional. You want the later revision to appropriate
some of the time interval currently associated with the earlier
revision.

**Steps:**

1.  Navigate to the "Manage Sites" page (e.g. Sites -\Manage Sites).

2.  Find the site you wish to edit in the site table and click on the
    "Edit" button (i.e., The Pencil icon). This will bring you to the
    "Edit Site" form.

3.  The "Revision Timeline" located towards the bottom of the page shows
    a visualization of existing site revisions. The highlighted blue bar
    represents the site revision currently being edited.

4.  In the "Date Range" section near the top of the page, edit the
    "Active Date" as needed.

5.  Click the "Update" button in line with the "Active Date" field.

6.  At this point you will see a warning about the pending update. If
    any associated records will be moved the warning message will
    include that information.

7.  Click the "Continue" button.

8.  You should see a success message and the Revision timeline chart
    should have an additional horizontal bar.

9.  Click continue again to navigate to the site edit page and make any
    changes to the newly created revision. The newly created revision is
    pre-populated with values from the previously existing site revision
    records. For instance, the "Site Name" may have a value of "copied
    from Site Revision one". User's will most likely want to edit this
    along with site coordinates and other values.

<div id="merge-sites"></div>

**Results**: The date range values of both site revisions have been
updated. Any associated records that were located in the "overlap"
will now be linked to the second site revision.

---

### **Merge two date-adjacent sites.**

**Scenario**: Your agency mistakenly created two site revisions for a
given date period. You want all records associated with the earlier site
to be associated with the second site revision and you want the first
site revision deleted.

**Steps:**

1.  Navigate to the "Manage Sites" page (e.g. Sites -\Manage Sites).

2.  Find the site you wish to keep in the site table and click on the
    "Edit" button (i.e., The Pencil icon). This will bring you to the
    "Edit Site" form for that site revision.

3.  Edit the site revision's "Active Date" to have the same value as the
    previous (unwanted) revision's "Active Date". The system will not
    allow you to surround an existing revision's date values (i.e., edit
    the second revision's "Active Date" to a value prior to the previous
    revision's "Active Date"), but lining up these revision's active
    dates exactly is allowed. Note: This operation will not work with
    empty/blank dates. In the case of a "empty" site date users would
    need to edit the previous (unwanted) revision's date field to an
    actual/existing date first.

4.  Click the "Update" button in line with the "Activate Date" field.

5.  At this point you will see a warning about the pending update. If
    any associated records will be moved the warning message will
    include that information.

6.  Click the "Continue" button.

7.  You should see a success message and the Revision timeline chart
    should no longer contain a bar for the first site revision.

**Results**: After a successful update, there is a single site
revision covering the entire time interval, all associated records
have been associated with that revision, and the unwanted site
revision is deleted. If needed, the existing site revision's date
fields can now be edited to cover a wider range of time.

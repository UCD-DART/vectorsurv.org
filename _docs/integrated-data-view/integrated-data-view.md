---
title: Integrated Data View
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/data-view
---

View multiple record types in one place. The Integrated Data View allows users to see different record types on one page in both table and map form. You can adjust the size of each panel by dragging the handle that divides the map and table views.

![Integrated Data View Page](/assets/images/docs/integrated-data-view.png)

## Data Filters

![Data View record Filters](/assets/images/docs/data-view-record-filters.png)

**Date**: Lets you select a custom timeframe to search for records. Click the refresh button ![Refresh Button](/assets/images/docs/refresh-btn.png) to fetch the relevant data.

**Data Settings**: Clicking on the gear ![Data Setting Icon](/assets/images/docs/gear-btn.png) icon will open a settings modal where you can select which record types to show in the tables and on the map. Click **Apply** to fetch new record types or **Cancel** to leave the settings unchanged.

## Tables

After selecting the data, use the tabs to switch between the data tables for the included data.

![Data Table](/assets/images/docs/integrated-data-view-tables.png)

- **Zoom To Record on Map**: Clicking on a row in the table will cause the map to pan to the relevant record. So, clicking on the row for Arthro Collection #10 in the table pictured above would cause the map to pan & zoom until the associated marker was centered in the view.

- **Sorting**: Click on column headers to sort data.

- **Filtering**: If there are more than 5 records in a table, a search field will appear allowing the user to filter records by any entered text.

- **Pagination**: If there are more than 5 records in a table, a pagination selector will appear at the bottom allowing users to page through data.

- **Action Buttons**: If the user has the ability to manage data, they will see the following icons.
  - Clicking the **Delete icon** ![Red trash can icon](/assets/images/docs/action-button-delete.png) in a row allows users to delete the associated record.
  - Clicking the **Edit icon** ![Pencil icon](/assets/images/docs/action-button-edit.png) will open a new tab to view and/or edit the associated record.

## Map

After selecting the date filter and record types, relevant data will appear on the map.  
**Note:** The currently selected table tab determines which record type is displayed on top in the map view.

![Data Table](/assets/images/docs/integrated-data-view-map.png)

- **Map Controls**:

  - **Recenter**: The recenter button ![Recenter Button](/assets/images/docs/recenter-btn.png) will refocus the map to encompass all existing data features. If there are no data features on the map, clicking this button will pan the view to the user's current agency location.
  - **Geocoder**: The geocoder tool allows you to quickly search for and zoom to an address or location on the map. Clicking the geocoder icon ![Magnifying Glass](/assets/images/docs/magnifying-glass.png) opens a search bar where you can enter an address or place name.

  ![Geocoder](/assets/images/docs/geocoder.png)

  - **View**: The view control ![View Control](/assets/images/docs/map-view-control.png) allows you to switch between different map views, such as Streets and Satellite. Hovering over the view control icon displays a popup with available options.

  ![View Control](/assets/images/docs/map-view-control-radio-btns.png)

  - **Zooming**: You can zoom in and out on the map using your mouse wheel or trackpad. Alternatively, use the standard **+** and **–** buttons located on the map interface to control the zoom level.

- **Popup Information**: Clicking on a map feature will cause a popup to appear with relevant details about the record. If there are multiple records at the location, a table of data will appear in the popup.

![Collection Cluster Popup](/assets/images/docs/application-popup-DV.png) ![Collection Cluster Popup](/assets/images/docs/collection-cluster-popup-DV.png)

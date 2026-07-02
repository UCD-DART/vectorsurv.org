---
title: Population Classification
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/site/pop-class
---

Assign Urban, Suburban, and Rural population classifications to multiple sites at once. Population classifications are used by various calculators and reports throughout VectorSurv.

## Visibility Filters

Use the **Visibility Filters** section to control which sites are displayed in the table and on the map.

- **Urban / Suburban / Rural / Unassigned**: Show or hide sites with the selected population classifications.
- **Show Prior Revisions of Site Codes**: Displays deactivated site revisions that are normally hidden.

These filters only affect which sites are displayed. They do not modify any population classifications or pending changes.

---

## Site Table

The site table displays a row for each site, including the current and pending population classifications for each site.

### Table Features

- **Current Population**: Displays the site's currently assigned population classification.
- **Updated Population**: Select a new population classification. Changes are staged until **Save** is clicked.
- **Zoom To Site**: Clicking a row pans and zooms the map to the selected site.
- **Sorting**: Click a column header to sort the table.
- **Filtering**: Use the search box to filter sites by code, name, or other displayed values.
- **Pagination**: Navigate between pages when more sites are available than can be displayed at once.

### Automatic Classification

Population classifications may also be assigned automatically. Note that the system may not be able to automatically classify some sites.

- **Auto**: Automatically suggests a population classification for an individual site when one can be determined.
- **Auto-classify Unassigned Sites**: Automatically suggests population classifications for all eligible unassigned sites.

---

## Map

The map provides another way to review and update population classifications.

### Map Controls

- **Recenter**: Centers the map on all displayed sites.
- **Geocoder**: Search for an address or location.
- **View**: Switch between Streets and Satellite imagery.
- **Zooming**: Use the mouse wheel, trackpad, or the **+** and **−** controls to zoom.

### Site Popups

- Clicking a site marker opens a popup showing the site's details.
- Population classifications can be updated directly from the popup.
- When many nearby sites exist, markers are grouped into clusters to improve map performance.
- If multiple sites occupy the same location, clicking the cluster displays a table allowing each site's classification to be updated individually.

### Polygon Assignment

The polygon tool allows multiple displayed sites to be updated at once.

1. Select the desired population classification.
2. Draw a polygon around one or more sites.
3. All enclosed displayed sites will receive the selected pending population classification.

The polygon is temporary and is removed after the operation completes.

---

## Saving Changes

Changes made on this page are staged locally and are not applied until **Save** is clicked.

A warning is displayed whenever there are unsaved updates.

Click **Reset** to discard all pending changes and restore the page to its last saved state.

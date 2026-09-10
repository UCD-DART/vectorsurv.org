---
title: Site Groups
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/site/group/group
---

Create and manage reusable groups of sites. Site groups make it easier to select commonly used sets of sites when running calculators and other VectorSurv workflows.

## Group Details

Provide the following information when creating or editing a site group.

- **Name (required)**: A descriptive name for the site group.
- **Comments (optional)**: Additional notes describing the purpose of the site group.
- **Share Group**: Allows other users within your agency to view and edit the site group.

---

## Agency Selection

Users with access to multiple agencies can choose which agencies' sites are available for selection.

- Select one or more agencies from the agency list.
- Click **Update Site List** to load sites from the selected agencies.
- Sites that are already part of the site group remain selected even if their agency is no longer included in the current agency selection.

---

## Site Tables

Use the **Selected Sites** and **Unselected Sites** tables to manage which sites belong to the group.

- **Selected Sites**: Displays the sites currently included in the group.
- **Unselected Sites**: Displays sites that are not currently included in the group.

### Table Features

- **Zoom To Site**: Clicking a row pans and zooms the map to the selected site.
- **Sorting**: Click a column header to sort the table.
- **Filtering**: Use the search box to filter sites by code, name, or other displayed values.
- **Pagination**: Navigate between pages when more sites are available than can be displayed at once.
- **Show Prior Revisions of Site Codes**: Displays deactivated site revisions that are normally hidden from the Unselected Sites table.

Sites may be added or removed using the table action buttons or directly from the map.

---

## Map

The map provides another way to review and manage the sites in the group.

### Map Controls

- **Recenter**: Centers the map on all displayed sites.
- **Geocoder**: Search for an address or location.
- **View**: Switch between Streets and Satellite imagery.
- **Zooming**: Use the mouse wheel, trackpad, or the **+** and **−** controls to zoom.

### Site Selection

- Clicking a site marker opens a popup showing site details.
- Sites can be selected or unselected directly from the popup.
- When many nearby sites exist, markers are grouped into clusters to improve map performance.
- If multiple sites occupy the same location, clicking the cluster displays a table listing each site.

### Polygon Selection

The polygon tools allow multiple sites to be updated at once.

- **Select Sites**: Draw a polygon to add all enclosed displayed sites to the group.
- **Unselect Sites**: Draw a polygon to remove all enclosed displayed sites from the group.

The polygon is temporary and is removed after the operation completes.

---

## Saving Changes

Changes made to the site group are not saved until **Save** is clicked.

Click **Reset** to discard any unsaved changes and restore the last saved version of the site group.

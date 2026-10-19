---
title: Susceptible Colonies
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/resistance/susceptible-colony
---

Create and edit susceptible mosquito colonies for use in bottle bioassays. Existing colonies can be selected as mosquito sources when entering bottle bioassay results.

## Colony Details

- **Name (required)**: Colony name.
- **Species (required)**: Mosquito species raised.
- **Year (required)**: The year the colony was established.
- **Shareable with all agencies in state**: Allows users in other agencies within your state to select the colony for their bottle bioassays. Each shared colony in a state must have a unique name.

---

## Location

Location information is optional. Use **Spatial Type** to specify how the colony's location is recorded.

- **Site**: Select an existing site to use its location information.
- **One-off Location**: Enter a location directly using the map.
- **Unknown**: Leave the colony's location unspecified.

### Site

Use **Site Code** to search for and select an existing site.

Selecting a site copies its location, shape, and coordinate precision into the colony form. Only the location information is saved with the colony; the association with the selected site is not retained.

### One-off Location

Use the map to draw the colony's location or enter latitude and longitude coordinates.

- **Latitude / Longitude**: Enter coordinates for a point location. Must present as a pair.
- **Precision**: Used to specify the level of certainty in the colony coordinates.

The map supports point orpolygon locations.

---

## Manage Colonies

The **Manage Colonies** table lists your colonies and your agency's shared colonies.

### Table Features

- **Sorting**: Click a column header to sort the table. By default, colonies are sorted alphabetically by name.
- **Filtering**: Use the search box to filter colonies by ID, name, species, year, or sharing status.

### Action Buttons

![Pencil icon](/assets/images/docs/action-button-edit.png): Open the selected colony in the form above to view or modify its details.

![Red trash can icon](/assets/images/docs/action-button-delete.png): Delete the colony.

---

## Saving Changes

Click **Save** to create a new colony.

When editing an existing colony, click **Update** to save your changes.

- **Clear form**: Clears the form and starts a new colony entry.
- **Reset**: Discards unsaved changes and restores the form to its previous state.

---

## Colonies Created from Bottle Bioassays

When entering a [Bottle Bioassay]({{ site.baseurl }}/docs/resistance/v5/bottle-bioassay), you can select an existing colony or enter a new colony name.

Entering a new name creates a colony record that can be selected in future bottle bioassays. Records created this way may be missing information found on the Susceptible Colonies form.

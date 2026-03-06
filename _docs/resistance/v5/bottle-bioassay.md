---
title: New Bottle Bioassay
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/resistance/bottle-bioassay
---

Use this page to import new bottle bioassay results into VectorSurv.

## Bottle Bioassay Details

- **Test Date** (required): The date this bottle bioassay test was conducted. Date format is based on the settings under [Account Preferences]({{ site.baseur1 }}/docs/settings/account-preferences).
  - **Include time?**: Toggle this switch to include the test start time. When enabled:
    - **Test Start Time**: Enter the specific time the test began
    - **Timezone**: Select the timezone for the test time. Click the timezone link to change if needed. Default timezone is based on the settings under [Account Preferences]({{ site.baseur1 }}/docs/settings/account-preferences)
- **Tested By**: The name of the person who conducted this bottle bioassay test.
- **Name**: Give this bottle bioassay an optional custom name. If no custom name is provided, tests will be labeled using this format: `Population Name(s) - Species – Ingredient + Dose(s) – Date` (Date format set through [user preferences]({{ site.baseurl }}/docs/settings/account-preferences/))
  - ex: "CSUF - Cx. pipiens s.l. – Pyrethrum 15ug, PBO 400ug – 07/02/2024"
- **Comments**: Add any description of the bottle bioassay performed or notes regarding this test.

## Ingredients

Add up to 3 ingredients (materials and/or synergists) used in this bioassay. At least one ingredient is required.

For each ingredient:

- **Ingredient** (required): Select the material or synergist from the dropdown. Options are grouped into Materials and Synergists and sorted alphabetically.
- **Dose**: The dose of the ingredient used in micrograms.
- **Lot**: The lot number for this batch of ingredient.

## Species

- **Species** (required): Select the mosquito species that was tested. Start typing to filter the list. The list of species in the dropdown can be
  adjusted through the Available Species settings on the [arthropod configuration page]({{ site.baseurl }}/docs/arthropod/trap-types/).
- **Mosquito Source Type** (required): Choose whether the tested mosquitoes were:
  - **Field**: Field-collected mosquitoes
  - **Colony**: Laboratory colony mosquitoes

  **Note**: Changing the source type will clear any existing source entries.

### Field-Collected Sources

For field-collected mosquitoes:

- **Generation** (required): Enter the generation number (e.g., F0, F1, F2). The "F" prefix is automatically added.

For each source (you can add multiple sources):

- **Source Name**: An optional name to identify this collection.
- **Collection Date Start**: The date collection started / trap was set (optional).
- **Collection Date End** (required): The date the specimens were collected.
- **Location** (required): Mark the collection location on the map by clicking on the map to place a marker (The map marker can be dragged to adjust the position) or entering latitude and longitude coordinates.

### Colony Sources

For colony mosquitoes:

- **Colony** (required): Start typing to filter the list of existing colonies for your agency. If none are found, a new colony entry will be created.

## Calculation Details

- **CDC Diagnostic Time**: Enter the time (in minutes) at which mortality should be assessed according to CDC guidelines for this material. This is used for resistance calculations.
- **Control Mortality**: _(Legacy data only)_ For older records, this shows the manually entered percent of mosquitoes that died in the control bottle. This field is automatically calculated from control bottle data in new submissions.

## Bottles and Mortality Data

The bottles table displays your mortality count data with bottles as columns and time points as rows.

### Table Settings

This section is open by default. You may set it to be hidden by default by checking the Keep Settings Closed by Default box. Clicking on the gear icon will toggle this section open or closed, but does not affect the default settings.

#### Test Defaults

- **Default Bottle Counts**: Set the default number of test and control bottles to add when creating a new bioassay. This only applies to new forms, not when editing existing data.
- **Default Time Interval**: The time (in minutes) between mortality counts when adding new time series rows. This affects the time value suggested when clicking "Insert time point below."

- **Time Series Preset**: Choose how time points are initialized:
  - **CDC Default**: Uses the standard CDC time series (0, 5, 10, 15, 30, 45, 60, 75, 90, 105, 120 minutes)
  - **Custom**: Define your own time series by entering comma-separated values in ascending order (e.g., "0, 15, 30, 45, 60")
    - Click **Save Configuration** to apply your custom time series
    - Once saved, this becomes your default for future bioassays

  **Note**: Changing the time series preset will clear all existing survival count data.

#### Keyboard Configuration

- **Tabbing Direction**: Choose how the Tab key navigates between cells:
  - **Tab down columns** (default): Tab moves down within a column, then to the next column
  - **Tab across rows**: Tab moves across the row, then down to the next row

- **Keyboard Shortcuts**:
  - **Shift + ↓**: Copy the current cell's value down to the cell below (won't overwrite manually entered data)
  - **Arrow Keys**: Navigate between cells within the Alive/Dead areas
  - **Alt ⌘ + ↑**: Jump up to the last filled cell in the current column
- **Mouse**:
  - **Click and drag down**: Fill remaining cells with the starting cell's value (won't overwrite manually entered data)

### Table Structure

#### Bottle Columns

- **Replicate Bottles**: Bottles containing tested ingredients. Displayed first (left side of table)
  - Click the + to add a bottle
  - Click the X to remove a bottle
- **Control Bottles**: Displayed after test bottles (right side of table)
  - Click the + to add a bottle
  - Click the X to remove a bottle
  - Click the pencil icon to edit control type (acetone or synergist)

#### Bottle Configuration Rows

- **Starting Count** (required): The initial number of mosquitoes placed in each bottle at the start of the test.

- **Female Count**: Optional count of female mosquitoes in the bottle (if sexed).
- **Male Count**: Calculated as Starting Count minus Female Count

#### Time Series Rows

Each row represents a time point (in minutes) at which mortality was assessed.

- **Time (min)**: The time in minutes from the start of the test. Click the time value to edit it.
- **Alive/Dead**: Count of mosquitoes still alive/dead at that time point. When you enter either Alive or Dead count, the other field automatically calculates based on the Starting Count. You can enter data in whichever column is more convenient.

#### Managing Time Points

- **Insert time point below**: Click the + icon next to any time point to add a new row below it. The suggested time will be based on your Default Time Interval setting.
- **Delete time point**: Click the trash icon to remove a time point row.

**Validation**: Time points must be in ascending order and cannot be duplicated.

## Saving Your Work

The form offers multiple save options accessed via the save button dropdown:

- **Save**: Saves the bioassay and navigates to the saved record detail page.

- **Save & Add: New**: Saves the bioassay and clears the form for a new entry, keeping only:
  - Test Date
  - Include time setting
  - Tested By
  - Bottle table structure (with data cleared)

- **Save & Add: Same Ingredients**: Saves the bioassay and starts a new entry keeping:
  - Test Date
  - Include time setting
  - Tested By
  - All ingredients
  - Comments
  - Bottle table structure (with data cleared)

  **Use this when testing the same materials on different mosquito populations.**

- **Save & Add: Same Sources**: Saves the bioassay and starts a new entry keeping:
  - Test Date
  - Tested By
  - Include time setting
  - Species
  - All sources
  - Mosquito source type
  - Generation
  - Comments
  - Bottle table structure (with data cleared)

  **Use this when testing different materials on the same mosquito population.**

Your preferred save option is remembered and becomes the default for future submissions.

- **Clear** Resets the form to empty state

## Editing Existing Bioassays

When editing an existing bottle bioassay:

- The save options are replaced with a single **Update Bioassay** button
- The **Reset** button will restore the form to the last saved values

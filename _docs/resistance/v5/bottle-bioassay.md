---
title: New Bottle Bioassay
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/resistance/bottle-bioassay
---

Use this page to enter bottle bioassay results into VectorSurv.

## Bottle Bioassay Details

- **Test Date** (required): The date the bottle bioassay test was conducted. Future dates are not allowed. Date format is based on [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
  - **Include time?**: Toggle this switch to include the test start time.
    - **Test Start Time**: Enter the time the test began.
    - **Timezone**: Select the timezone for the test time. The default is based on [Account Preferences]({{ site.baseurl }}/docs/settings/account-preferences).
- **Test By**: The person who conducted the test.
- **Test Name**: Test name. The field displays a suggested name based on the available test details.
- **Comments**: Add a description of the bioassay or other notes about the test.

## Ingredients

At least one ingredient or formulated product used in the bioassay is required. Add up to three.

For each entry:

- **Ingredient / Formulated Product** (required): Select a material, synergist, or formulated product. Materials and synergists are grouped in the ingredient list. Formulated products can be selected separately and may include EPA registration numbers in their descriptions when available.
- **Dose** (required): The dose in micrograms per bottle (µg/bottle). Must be greater than zero.
- **Lot**: Lot number for this batch of ingredient.

## Species

- **Species** (required): Select the mosquito species tested. Start typing to filter the list. Available species can be adjusted through the [arthropod configuration page]({{ site.baseurl }}/docs/arthropod/trap-types/).
- **Mosquito Source Type** (required): Choose **Field** for field-collected mosquitoes or **Colony** for colony-raised mosquitoes.

Changing mosquito source type removes existing source entries.

### Field-Collected Sources

- **Generation (F)** (required): Enter the generation number (for example, F0, F1, F2). The F prefix is displayed by the form.

You can add multiple field sources. For each source:

- **Source Name**: An optional name identifying the collection.
- **Collection Date Start**: The date the collection began or the trap was set.
- **Collection Date End** (required): The date the specimens were collected. This cannot be in the future or after the test date, or precede the collection start date.
- **Location** (required): Mark the collection location on the map or enter latitude and longitude coordinates. You can drag the marker to adjust its position.

At least one source is required.

### Colony Sources

- **Source Name**: Select an existing colony from your agency or enter a new colony name. Entering a new name will create a new colony record that can be used in future bottle bioassays. Additional colony details can be completed through the [Susceptible Colonies form]({{ site.baseurl }}/docs/resistance/v5/susceptible-colony).

## Calculation Details

Use **Diagnostic Time** to specify how the diagnostic time for the bioassay is determined.

- **CDC Diagnostic Time**: Enter the CDC recommended diagnostic time in minutes. If provided, the value must match one of the observation times in the bottles table.
- **Linked Colony Test**: Select an eligible susceptible colony test to use its calculated diagnostic time. Available tests are based on the current species, test date, and ingredients and doses, which must be present before another test can be linked.
- **Diagnostic**: For colony tests, this option will calculate and save the first time value at which all replicates achieve 100% mortality. For field tests, this value may provided to indicate that the diagnostic time has no linked source. If provided, the value must match one of the observation times in the bottles table. If no value is provided for this option, the diagnostic time will be calculated from the bottle results.
- **Control Mortality**: _Legacy data only._ When editing an older record that contains a manually entered control mortality percentage, that value can be viewed or updated. For new records, control mortality is calculated from the control bottles.

## Bottles and Mortality Data

The bottles table displays mortality data, with bottles as columns and observation times as rows. Replicate bottles appear before control bottles.

### Table Settings

Click the gear icon to expand or collapse the settings. You can also choose to keep the settings closed by default.

#### Test Defaults

- **Default Bottle Counts**: Set the number of replicate and control bottles initially added to a new bioassay.
- **Default Time Interval**: Set the interval in minutes used to suggest a time when inserting a new observation after the final time point.
- **Time Series Preset**: Choose how observation times are initialized:
  - **CDC Standard**: Uses 0, 5, 10, 15, 30, 45, 60, 75, 90, 105, and 120 minutes.
  - **Custom**: Enter comma-separated time points in ascending order (for example, `0, 15, 30, 45, 60`), then save the configuration for future bioassays.

Changing the time-series configuration can clear existing survival counts.

The default bottle count and time-series preset controls are available when creating a new bioassay. You can still add or remove bottles and edit observation times when editing a saved bioassay.

#### Keyboard Configuration

- **Tabbing Direction**: Choose whether Tab follows the standard navigation order or moves down the cells of a column before moving to the next column.
- **Shift + ↓**: Fill the cell below with the current cell's value. Does not overwrite manually entered data.
- **Arrow Keys**: Navigate between cells within the Alive and Dead areas.
- **Alt ⌘ + ↑**: Jump to the last filled cell in the current column.
- **Click and drag down**: Fill additional cells with the starting value. Does not overwrite manually entered data.

### Table Structure

#### Bottle Columns

- **Replicate Bottles**: Bottles containing the tested ingredients. Click **+** to add a bottle or **X** to remove one.
- **Control Bottles**: Bottles used as controls. Click **+** to add a bottle and choose **Acetone** or **Synergist** as the control type. Use the pencil icon to change an existing control's type or **X** to remove the bottle.

A bottle bioassay requires at least one replicate and one control.

#### Bottle Configuration Rows

- **Starting Count (T)** (required): Total number of mosquitoes in each bottle.
- **Female Count (F)**: Female mosquito count. Cannot exceed starting count.
- **Male Count (M)**: Calculated as Starting Count minus Female Count.

#### Time Series Rows

Each row represents an observation time, in minutes after the test began, at which mortality was assessed.

- **Time (min)**: Click a time value to edit it. Times must be whole numbers in strictly ascending order, with no duplicates.
- **Alive / Dead**: Enter the number of mosquitoes alive or dead at that time. Entering one value automatically calculates the other from the Starting Count. Counts can be zero, and alive count cannot exceed starting count.

#### Managing Time Points

- **Insert time point below**: Click the **+** next to a time point. When inserting between two existing times, the new time is suggested at their midpoint. After the last time point, the suggested time is based on your Default Time Interval.
- **Delete time point**: Click the trash icon to remove a row.

You must keep at least one time point. A new time cannot be inserted between consecutive times that are only one minute apart.

## Saving Your Work

The form offers multiple save options via the save button dropdown. Your last-used save option is remembered for future submissions.

- **Save**: Saves the bioassay and opens the saved record in the form.
- **Save & Add: New**: Saves the bioassay and prepares a new entry, retaining tester and test date settings.
- **Save & Add: Same Ingredients**: Saves the bioassay and prepares a new entry, retaining tester, ingredients, comments, and test date settings. Use when testing the same materials on different mosquito populations.
- **Save & Add: Same Sources**: Saves the bioassay and prepares a new entry, retaining tester, species, mosquito source type, sources, generation, comments, and test date settings. Use when testing different materials on the same mosquito population.

All **Save & Add** options retain the bottle structure and observation times and clear bottle counts and survival results.

Selecting an option makes it the default for subsequent submissions.

Click **Clear** to return the form to its defaults.

## Editing Existing Bioassays

Open an existing record through the [Manage Bottle Bioassays]({{ site.baseurl }}/docs/resistance/v5/bottle-bioassay-manage) page to review and edit its details and results.

- **Update** saves changes to the existing record.
- **Reset** discards unsaved edits and restores the last loaded values.

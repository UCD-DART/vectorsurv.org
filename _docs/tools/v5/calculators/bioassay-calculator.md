---
title: Bottle Bioassay Calculator
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/tools/calculators/bottle-bioassay
---

Use this calculator to estimate survival curves and knockdown times (KD50 and KD95) from saved bottle bioassay test results.

## Available Tests

The **Available Tests** table displays bottle bioassays from your current agency, along with susceptible colony tests from other agencies in your state. By default, tests are sorted by date (most recent first), then by ID (highest first).

Each test row displays:

- **ID**: Test identifier. If you have permission to view this test, ID is a clickable link that opens the test details in a new tab.
- **Agency**: The code for the agency the test belongs to.
- **Name**: Test name.
- **Date**: Test date in your preferred format.
- **Species**: Mosquito species tested.
- **Source Type**: Whether the mosquitoes were field-collected or from a colony.
- **Sources**: Collection sources or colony names.
- **Paired References**: Indicates when a test has a susceptible colony or CDC diagnostic-time reference.
- **Ingredients**: Materials, synergists, or formulated products used, with doses.

### Sorting and Searching

- **Sorting**: Click a column header to sort the table. Click again to reverse the sort order.
- **Searching**: Use the search box to find tests by ID, agency, name, date, tester, species, source type, sources, or ingredients.

### Filtering Available Tests

Use **Filter Fields** to select which filters are displayed. Choose filter values, then click the refresh-table button to apply them.

Available filters include:

- **Agency**: Select one or more agencies.
- **Paired Reference**: Filter tests based on CDC or Linked Colony diagnostic time source.
- **Test Name**: Filter by test name.
- **Tested By**: Filter by the person who conducted the test.
- **Ingredients**: FIlter by ingredient(s).
- **Source Name**: Filter by collection source or colony name.
- **Species**: Filter by species tested.
- **Date**: Specify a date range.
- **Dose**: Filter by ingredient dose in micrograms.

When filtering by dose, use the range slider to specify minimum and maximum doses.

Multiple values within most filters can be selected. When using several different filters, tests must satisfy each filter's conditions. When multiple ingredients are selected, tests must contain all selected ingredients.

---

## Selecting Tests

Click **Select Test** in the Available Tests table to add a bottle bioassay to the **Selected Tests** table.

Selected tests remain visible in the Available Tests table with highlighted styling.

- You can select up to **7 tests** for a single calculation.
- To remove a test, use its deselect action in either table.
- Use the Selected Tests search box to find records within your selection.

The number of selected tests is displayed below the tables.

**Note:** All selected tests are included when running a calculation, including those hidden by a search or filter.

---

## Running Calculations

After selecting one or more tests, click **Calculate** to begin the analysis.

A progress indicator displays the calculation status and elapsed time.

- **Cancel calculation(s)**: Stop waiting for the current calculation. The calculation may continue processing on the server.
- **Recalculate**: Run a new calculation using the currently selected tests. Previous results are cleared when a new calculation begins.

Changing your current agency clears the selected tests, filters, and calculation results.

---

## Viewing Results

### Calculation Results Table

After a successful calculation, the **Calculation Results** table displays the calculated statistics and mortality results for each selected test.

The table includes:

- **ID**: Test identifier.
- **Agency**: Agency code.
- **Name**: Test name.
- **Date**: Test date.
- **Species**: Mosquito species.
- **Source Type**: Whether the mosquitoes were from a colony or field-collected.
- **Sources**: Collection sources or colony names.
- **Ingredients**: Materials, synergists, or formulated products, with doses.
- **KD50 (ci)**: Estimated time to 50% knockdown, with confidence interval.
- **KD95 (ci)**: Estimated time to 95% knockdown, with confidence interval.
- **Diagnostic Time**: Diagnostic time associated with the test.
- **Control Mortality**: Control mortality returned by the calculation.

Additional columns display mortality percentages at each exposure time recorded in the calculated tests. These columns vary depending on the time points in the selected bioassays.

KD estimates and confidence intervals are displayed to two decimal places. Results that cannot be calculated may appear as N/A or blank values.

### Table Features

- **Sorting**: Click a column header to sort the results.
- **Searching**: Use the search box to filter results by test details, calculated values, or mortality observations.
- **Pagination**: Navigate between pages or adjust the number of results displayed per page.

---

## Viewing the Graph

Click **View Graph** to open a chart displaying mortality curves for the calculated tests.

The graph shows:

- **X-axis**: Exposure time in minutes.
- **Y-axis**: Percent knockdown.
- **Test Curves**: Each calculated test is represented by a line.
- **Control Mortality**: Control mortality observations are displayed where available.
- **Diagnostic Time**: Markers identify diagnostic times, including linked colony diagnostic references where available.

Tests are labeled using their names or a description based on their sources, species, and ingredients.

### Graph Options

- **Corrected**: Display Abbott-adjusted mortality values where available. Perhaps this is where Abbott's correction could be further explained.
- **Uncorrected**: Display mortality values without Abbott's correction.
- **Toggle Lines**: Click legend entries to show or hide individual test curves.
- **Download Screenshot**: Download the displayed graph as a PNG image.

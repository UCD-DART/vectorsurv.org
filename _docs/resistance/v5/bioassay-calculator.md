---
title: Bottle Bioassay Calculator
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/tools/calculators/bottle-bioassay
---

Use this calculator to estimate survival curves and knockdown times (KD50 and KD95) from bottle bioassay test results.

## Available Tests

The **Available Tests** table displays all submitted bottle bioassay tests from your agency, along with tests from state colonies that are available for analysis. By default, tests are sorted by date (most recent first), then by ID (highest first).

Each test row displays:

- **ID**: Test identifier. If you have permission to view this test, the ID is a clickable link that opens the test details in a new tab.
- **Agency**: The code for the agency the test belongs to
- **Name**: Custom name for the test (if provided)
- **Date**: Test date in your preferred format
- **Species**: Mosquito species tested
- **Source Type**: Whether mosquitoes were field-collected, from a colony, or lab-reared
- **Sources**: Collection sites or colony names
- **Ingredients**: Materials and synergists used, with doses

### Sorting Available Tests

Click any column header to sort the table by that field. Click again to reverse the sort order.

### Searching Available Tests

Use the search box above the table to filter tests.

### Pagination

The Available Tests table displays 25 tests per page by default. Use the pagination controls at the bottom to:

- Change the number of items displayed per page
- Navigate between pages

Your items per page preference is saved for future sessions.

## Selecting Tests

To select a test for calculation, click the **+** (plus) icon in the actions column. The test will:

- Be added to the **Selected Tests** table below
- Remain visible in the Available Tests table with highlighted styling

**Selection Limit**: You can select up to 10 tests at a time. If you try to select more, you'll see a warning message. Deselect a test before adding another.

To deselect a test, click the **−** (minus) icon in the actions column of either table. The test will be removed from the Selected Tests table and the highlighting will be removed.

The number of currently selected tests is displayed below the tables.

**Note**: When you run a calculation, it will process ALL selected tests, even if you've filtered the Selected Tests table with a search query.

## Running Calculations

Once you've selected at least one test (up to 10 tests), click the **Calculate** button to begin the analysis.

If you haven't selected any tests, you'll see a warning asking you to select at least one test.

## Viewing Results

### Results Table

After a successful calculation, the **Calculation Results** table displays:

**Static Columns:**

- **ID**: Test identifier (same as in selection tables)
- **Agency**: Agency code
- **Name**: Custom test name (if provided)
- **Date**: Test date
- **Species**: Mosquito species
- **Source Type**: If the mosquitoes were taken from a colony or field-collected sample(s)
- **Sources**: Field location or colony name, each source listed on a new line
- **Ingredients**: Materials and synergists with doses, each ingredient listed on a new line
- **KD50**: Knockdown time for 50% mortality (with confidence interval)
- **KD95**: Knockdown time for 95% mortality (with confidence interval)

**Dynamic Columns:**

Additional columns show percent mortality at each exposure time point recorded in the tests (e.g., 30 minutes, 60 minutes, 90 minutes, etc.). The specific time points displayed depend on the data in your selected tests.

### Viewing the Graph

Click the **View Graph** button to open a modal displaying mortality curves for all calculated tests.

The graph shows:

- **X-axis**: Exposure time (minutes)
- **Y-axis**: Percent mortality
- **Legend**: Each test corresponds to a line. If no test name is provided, tests will be labeled using this format: `Population Name(s) - Species – Ingredient + Dose(s) – Date` (Date format set through [user preferences]({{ site.baseurl }}/docs/settings/account-preferences/))
  - ex: "CSUF - Cx. pipiens s.l. – Pyrethrum 15ug, PBO 400ug – 07/02/2024"

**Graph Options:**

- **Toggle Lines**: Click legend items to show/hide specific test curves
- **Download**: Save the graph as an image file

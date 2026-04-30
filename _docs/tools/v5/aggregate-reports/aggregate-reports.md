---
title: Aggregate Reports
v5: true
gateway-url: https://gateway.vectorsurv.org/v5/tools/aggregate-reports
---

Quickly generate reports from your agency or from multiple agencies to compare arbovirus activity.

## Report Filters

Use the filters below to define which data is included in the report.

- **Report Type (required)**: Select the type of report to generate. The available filters and results will update based on the selected report.
- **Agencies (required)**: Choose the agency or agencies to include in the report. Multiple agencies can be selected.
- **Filter By (required)**: Choose which date is used to determine whether records are included in the report.
  - **Collection Date**: Records are included based on when the specimen was collected.
  - **Test Date**: Records are included based on when the specimen was tested.

  > **Note:** Previous versions of these reports used different date filtering rules. The v5 reports use the selected **Filter By** option.

- **Disease Week and Year (optional)**: Select a disease week and year to filter results to a specific reporting week. Selecting a disease week will automatically set the **From** and **To** date fields. Changing the year updates the **From** and **To** dates when a disease week is selected.

- **Date Range (From / To) (required)**: Enter the start and end dates for the report. The report will include records within the specified date range.

---

## Arthropod Pool Test Results

Summarizes mosquito pool testing results by test target (e.g., WNV, SLE).

Mosquito pools may be tested multiple times using different methods. VectorSurv applies an internal ranking of test methods to determine the final result for each pool and target.

- RTPCR results take priority over all other methods
- If multiple non-RTPCR tests exist, the most recent test is used
- Only the highest priority result is reflected in the report output.

### Tables

- **# of Pools**: Summary of all pools with test results in the selected date range, grouped by test target.
  - Each row represents a test target.
  - **# of Pools**: Total number of distinct pools tested for that target.
  - Status columns show how many pools are Positive, Negative, or Pending.

- **# of Pools By Agency**: Same as **# of Pools**, but grouped by collecting agency.
  - Each row represents a collecting agency and test target.
  - Counts reflect pools collected by that agency.

- **Positive Pool Details**: Detailed listing of pools with a confirmed positive result.
  - Each row represents one pool and one test target.
  - Includes collection details (agency, location, species, etc.) and test details (agency, method, date).

- **Pending Pool Details**: Same structure as Positive Pool Details, but for pools whose results are still pending.

- **# of Pools By Test Agency**: Summary grouped by testing lab, test method, and test target.
  - Each row represents a testing agency, method, and target.
  - Pools are attributed to the lab that produced the final result.

- **# of Pools By Multiple Test Agencies**: Lists pools that were tested by more than one agency.
  - Each row represents a unique combination of agencies.
  - The count shows how many pools were tested by that exact combination.

- **Pool Status Breakdown**: Tracks pools through the submission and testing workflow.

  | Column    | Description                                                |
  | --------- | ---------------------------------------------------------- |
  | Created   | Pools created during the selected date range               |
  | Submitted | Pools that have been submitted to a lab                    |
  | Received  | Pools that have been received by a lab                     |
  | Tested    | Pools that have at least one test result                   |
  | Untested  | Pools that were received but do not yet have a test result |

- **Test Panel Orders**: Shows how many pools were submitted by an agency to a lab.
  - Rows represent submitting agency and testing agency combinations.
  - Columns represent test panel codes.
  - Values show the number of pools for each combination.

  > **Note:** To avoid excluding untested pools, this table always uses collection date, regardless of the selected **Filter By** option.

---

## Sentinel Sample Test Results

Summarizes sentinel chicken testing results by test target (e.g., WNV, SLE).

### Result Prioritization

VectorSurv determines a single final result per sample using ranked test methods.

- PRNT (Plaque Reduction Neutralization Assay) (highest priority)
- WB (Western Blot)
- IFA (Indirect Immunofluorescence Assay)
- EIA (Enzyme Linked Immunoassay)

Only the highest priority result is reflected in the report output.

### Tables

- **# of Bands/Samples**: Summary grouped by test target that includes both sample-level and bird-level counts.

  | Column                        | Description                              |
  | ----------------------------- | ---------------------------------------- |
  | # of Samples                  | Total number of blood draws with results |
  | Positive / Negative / Pending | Counts of samples in each status         |
  | # of Bands                    | Number of unique birds with results      |
  | Band status columns           | Number of unique birds in each status    |

- **# of Bands/Samples By Agency**: Same as **# of Bands/Samples**, grouped by collecting agency.
  - Each row represents a collecting agency and test target.
  - Includes both sample-level and bird-level counts.

- **New Positive Sample Details**: Lists samples that represent the first confirmed positive result for a bird and target.
  - Each row represents one sample and one target.
  - Includes only first-time detections for each bird.

- **Positive Sample Details**: Lists all confirmed positive samples.
  - Includes both new and repeat positives.
  - Contains all rows from New Positive Sample Details plus additional records.

- **Pending Sample Details**: Lists samples whose results are still pending.

- **# of Samples By Test Agency**: Summary grouped by testing lab, test method, and test target.
  - Each row represents a testing agency, method, and target.
  - Counts reflect the final selected result for each sample.

- **# of Samples By Multiple Test Agencies**: Lists samples that were tested by more than one agency.
  - Each row represents a unique combination of agencies.
  - The count shows how many samples were tested by that exact combination.

---

> **Quick Tip:** If you need to review this documentation just click the help icon located in the title bar. ![Help Icon]({{ site.baseurl }}/assets/images/docs/help-icon.PNG)

---
title: Issues
gateway-url: https://gateway.vectorsurv.org/core/ppf/issue_manage
---

This page keeps track of potential mismatches in the data entered into the Gateway. The Gateway periodically checks many of an agency's records (sites, collections, pools) and attempt to flag potential "issues". Records that have been identified will appear in this table. Records that appear in this table will otherwise still behave as normal.

Records flagged by the system can be removed from this table in three ways:

1. The record can be resolved by clicking the _Submit as Resolved_ link in the table. This indicates to the system that the record exists as intended (for instance, a collection was knowingly made outside agency boundaries). Only users with edit privileges can resolve an issue.
2. When a record is edited, its potential issue status will be reset. If the data discrepancy still exists, the record will appear in the table again after the next sweep.
3. Deleted records do not appear in the table.

If your current agency has potential data issues, red dots will appear around the **Issues** tab at the top of the page. ![Issues]({{ site.baseurl }}/assets/images/docs/issues.PNG)

The **Manage Issues** table tracks multiple types of issues:

- Date issues are noted for collections and pools where the record was created in the gateway before its assigned collection date.
- Spatial issues are noted when coordinates for a [site]({{ site.baseurl }}/docs/site/ or [collection]({{ site.baseurl }}/docs/arthropod/collection) fall outside agency boundaries. If an agency has no boundaries in the Gateway, state boundaries are used instead.

The **Manage Issues** table displays information about each record with either a Spatial or Date issue. If a record has multiple potential issues, it will appear in the table for each type.

- **Record Name**: The name and ID of the record that was flagged.
- **Add Date**: The date the record was added to the Gateway.
- **Issue Description**: Whether this issue is Spatial or Date and a brief description of the issue.
- **Off By**: For date issues, this is the difference in days between the active date and the add date. For spatial issues, this is the distance from the record's coordinates to the agency's boundaries.
- **View/Edit**: Use this link to view and/or edit the record. Clicking the link will bring you to a filled-in page for the type of record that was flagged, similiar to editing a record from the [Collection Management]({{ site.baseurl }}/docs/arthropod/collection-manage) page, for example. A box at the top of the page will identify the issue(s) with this record and suggest possible actions. You can either click within the box to return to the **Manage Issues** page or click the **Update** button at the bottom of the page to save any changes.
  ![Issues box]({{ site.baseurl }}/assets/images/docs/issues-box.PNG)
- **Comments**: Click the ellipsis to add any comments about this issue. It is highly recommended to include comments if the record will be submitted as resolved (see below) to explain why the record is correct.
- **Actions**: Click the _Submit as Resolved_ link to indicate that this record appears as intended (for instance, the site is intentionally outside agency boundaries). This will remove the record from the **Manage Issues** table. It will also prevent the record from being flagged for the same issue in the future.

Records in the table can be filtered by name, date, type of issue, etc. using the search box below the table.
![Filter issues]({{ site.baseurl }}/assets/images/docs/filter-issues.PNG)

Note: It is recommended to handle site issues before collection issues. This is because collections may inherit site spatial issues, such that fixing or resolving a site's issues will remove its dependent collections from the **Manage Issues** table.

---
title: "VectorSurv Starting Guide"
permalink: /starting/
---

- [Starting with VectorSurv as a New Agency](#StartingOnVectorSurvAgency)

- [Starting with VectorSurv as a New User for an Existing Agency](#StartingOnVectorSurvUser)

- [VectorSurv Gateway vs. Sandbox](#VectorSurvSandbox)

- [Importing Data into VectorSurv](#ImportingData)

- [Exporting Data from VectorSurv](#ExportingData)

- [Data Access on VectorSurv](#DataAccess)

- [VectorSurv Citation](#VectorSurvCitation)

## Starting with VectorSurv as a New Agency {#StartingOnVectorSurvAgency}

Welcome to VectorSurv! VectorSurv is web-based software to enable data management and analysis by local and state public health agencies throughout the U.S. As the name suggests, we focus on data relevant to surveillance and control of vector-borne diseases, and all data are referenced by geographic location and date. For surveillance, the types of data we store are commonly called “environmental surveillance data” and include mosquito trap collections, tick collections, mosquito and tick pathogen testing, dead bird testing for West Nile virus, and sentinel chicken serological testing. For control, we store data on pesticide applications and pesticide resistance. We also provide tools to streamline reporting to CDC’s national databases, particularly ArboNet.

In order to start using VectorSurv as a new agency, initial information is required regarding the requesting agency and at least one agency manager of the requesting agency.

Required and optional onboarding information can be sent to ![Help Email].

**Agency Information:**

The following information regarding the requesting agency, mosquito control district, or health department is required before an agency can be added to VectorSurv. The only limiting factor regarding these four data elements is that the 4-letter agency code must be unique within the requesting agency's state. For example, if an agency within California has the agency code "WXYZ," no other agencies within California can use that specific agency code.

- Desired 4-letter Agency Code:

- Official Agency Name:

- Street Address (Street Address, City, Zip):

- County:

**Agency Manager(s) Information:**

In addition to the required agency information, at least one agency manager for each requesting agency is required at the time of onboarding. This person should be in a supervisory role with the authority to add and edit other users’ accounts and agency preferences on behalf of their agency. The person does not necessarily need to be the top-level manager of the entire agency. The following information regarding the agency manager is required.

- First Name:

- Last Name:

- Desired Username:

- User Email:

**Optional Information:**

Lastly, if available, it is beneficial to provide a shapefile or other GIS file that contains the requesting agency's spatial boundary definitions. If an agency spans an entire county, group of counties, or an entire state, VectorSurv only needs to know which counties the agency represents and can define the agency boundary from an existing county boundary data set.

Agency boundaries are not required to be unique or avoid overlap. For example, multiple agencies, such as a mosquito control district, a local public health agency, and a statewide public health agency, can all share the same geographic area. As another example, neighboring agencies may also overlap in certain border areas due to differences in services provided in the overlapping areas.

**Next Steps:**

Once the agency and at least one agency manager are added to the system, the VectorSurv Gateway emails the agency manager with a generated link that will allow the manager to create a password. The manager will then have immediate access to log into the VectorSurv Gateway (<https://gateway.vectorsurv.org/>) and will be able to add additional agency managers and users by navigating to [Settings] > [My Agency] > [Manage Users] > [Add New User]. Additionally, once access is granted, a good first step for users is to review their account preferences, including the user's preferred date format, time format, time zone, and latitude / longitude format. Account preferences can be set by navigating to [Settings] > [My Account] > [Account Preferences].

VectorSurv also offers a "playground" environment, known as the Sandbox (<https://sandbox.vectorsurv.org/>), where users are allowed to experiment with the various website features without any risks to the real data that has been entered into the VectorSurv Gateway. Data entered or features tested within the Sandbox environment do not persist as the Sandbox is reset each weekend to match the data in the Gateway. Once an agency is onboarded, agency users will be able to access the Sandbox the following week after the Sandbox is reset over the weekend.

VectorSurv staff have also produced reference materials that may be of assistance to new agencies as they get started on VectorSurv. The first is VectorSurv's documentation website that provides useful information on the VectorSurv Gateway and its various features (<https://vectorsurv.org/docs/>). Additionally, VectorSurv's YouTube channel contains previously recorded training videos on how to use the features of the VectorSurv Gateway (<https://www.youtube.com/channel/UCCtI2QiZKE32AtlaiAVzl-g>).

Lastly, feel free to reach out to ![Help Email] if any additional questions or concerns arise during the onboarding process. This email address reaches our programmers, data analysts, and administrators, which helps ensure that messages don’t get missed.

[Return to Top](#TableOfContents)

## Starting with VectorSurv as a New User for an Existing Agency {#StartingOnVectorSurvUser}

Welcome to VectorSurv! In order to be added to VectorSurv as a new user to an existing agency within VectorSurv, permission will need to be granted by the manager of the agency the new user is requesting access to.

VectorSurv's structure allows for agencies and agency managers to determine who is allowed to have access to their agency's data. Agency managers are able to add and remove users by navigating to [Settings] > [My Agency] > [Manage Users]. If a new individual would like to become a user for an agency, the best path forward is to reach out directly to the agency manager to request access.

In situations where the agency manager is not available to create new users or if identifying the agency manager is not possible, please reach out to VectorSurv at ![Help Email] to create a new agency manager or to identify the manager for the requested agency.

**Next Steps:**

Once the new user is added to the agency by the agency manager, the new user will then have immediate access to log into the VectorSurv Gateway (<https://gateway.vectorsurv.org/>) and will be able to set their own password by navigating to [Settings] > [My Account] > [Security Details]. Additionally, once access is granted, a good first step for users is to review their account preferences, including the user's preferred date format, time format, time zone, and latitude / longitude format. Account preferences can be set by navigating to [Settings] > [My Account] > [Account Preferences].

VectorSurv also offers a "playground" environment, known as the Sandbox (<https://sandbox.vectorsurv.org/>), where new users are allowed to experiment with the various website features without any risks to the real data that has been entered into the VectorSurv Gateway. Data entered or features tested within the Sandbox environment do not persist as the Sandbox is reset each weekend to match the data in the Gateway. Once a new user is onboarded, the user will be able to access the Sandbox the following week after the Sandbox is reset over the weekend.

VectorSurv staff have also produced reference materials that may be of assistance to new users as they get started on VectorSurv. The first is VectorSurv's documentation website that provides useful information on the VectorSurv Gateway and its various features (<https://vectorsurv.org/docs/>). Additionally, VectorSurv's YouTube channel contains previously recorded training videos on how to use the features of the VectorSurv Gateway (<https://www.youtube.com/channel/UCCtI2QiZKE32AtlaiAVzl-g>).

Lastly, feel free to reach out to ![Help Email] if additional questions or concerns arise during the onboarding process as a new user. This email address reaches our programmers, data analysts, and administrators, which helps ensure that messages don’t get missed.

[Return to Top](#TableOfContents)

## VectorSurv Gateway vs. Sandbox {#VectorSurvSandbox}

VectorSurv offers two separate software environments that may be of use to enrolled agencies, the VectorSurv Gateway and the VectorSurv Sandbox.

The VectorSurv Gateway (<https://gateway.vectorsurv.org/>) can be considered the "live" VectorSurv environment. Data entered to the VectorSurv Gateway will be stored permanently within the VectorSurv database, and changes made within the VectorSurv Gateway environment will persist to future login sessions. This environment is the main interface for managing and sharing all relevant data that is to be stored within the system. This ensures that users will continually have access to their data for future analysis or for it to be shared with relevant partners as determined by the agency.

The VectorSurv Sandbox (<https://sandbox.vectorsurv.org/>) is the system's "playground" environment. Data entered to the VectorSurv Sandbox are a copy of the VectorSurv Gateway’s data and settings through the previous week. Data in the Sandbox do not persist, as the Sandbox is reset each weekend to exactly match the data and settings that are found in the VectorSurv Gateway at the time of the reset. This environment aims to be a testing space where users are allowed to experiment with entering or importing data, changing settings, and using the various website features without any risks to the data that has been entered into the live VectorSurv Gateway. This ensures that users are able to try out all of the existing or newly released features of VectorSurv risk-free before using them within the VectorSurv Gateway.

[Return to Top](#TableOfContents)

## Importing Data to VectorSurv {#ImportingData}

In addition to adding data values directly through the VectorSurv Gateway user interface, VectorSurv allows for batch entry of various types of data through import processes. Data can be imported into VectorSurv in two separate ways.

**Excel (.xls) or CSV (.csv) File Imports:**

Newly collected and historic data not yet entered to VectorSurv can be imported to the VectorSurv Gateway through the use of Excel (.xls) or CSV (.csv) files formatted to match VectorSurv's data structure. The data formats required to import new data using Excel (.xls) or CSV (.csv) files can be found within VectorSurv's data import specifications file (<https://ucdavis.app.box.com/v/VS-Gateway-Import-Specs>).

Once the Excel (.xls) or CSV (.csv) file is correctly formatted for import, users can import files by navigating to [Tools] > [Data Tools] > [Data Import].

The following types of data are available to be imported through the VectorSurv Gateway's Excel (.xls) or CSV (.csv) file import process.

- Surveillance Sites
- Arthropod Collections
- Arthropod Collections (with species and gender structured in a spreadsheet-style format)
- Arthropod Pools
- Arthropod Pool Test Results
- Sentinel Bands
- Sentinel Band Bleeds
- Sentinel Band Bleed Test Results
- Pesticide Applications
- Application Technicians
- Application Mixes
- Application Equipment
- Application Source
- Tick Collections
- Tick Collections (with species and gender structured in a spreadsheet-style format)
- Tick Pools

The import process for Excel (.xls) or CSV (.csv) files can also be tested in the VectorSurv Sandbox (<https://sandbox.vectorsurv.org/>). As with all data entered to the VectorSurv Sandbox, data imported to the VectorSurv Sandbox does not persist as the Sandbox is reset each weekend. If the data import completes successfully in the VectorSurv Sandbox, that provides an indication that the same data can be imported into the live copy of the data on the VectorSurv Gateway if desired.

Assistance with the Excel (.xls) or CSV (.csv) file import process can also be provided by VectorSurv's staff when available. Please reach out to VectorSurv at ![Help Email] to request such assistance.

**Web Service Imports:**

Newly collected and historical data not yet entered into VectorSurv can also be imported to the VectorSurv Gateway through the use of VectorSurv's web service. This service is primarily intended for agencies with local in-house data applications or for agencies implementing custom code. The specifications for the web service import process can be found on our documentation website (<https://trac.vectorsurv.org/gateway/wiki/ImportWebService>).

To begin using VectorSurv's web service import process, an agency token is required to demonstrate that the import request has the proper authentication. Agency tokens can be generated by navigating to [Settings] > [My Agency] > [Agency Tokens]. Software vendors seeking to connect on behalf of a client agency would need to obtain a token from an agency manager at the client agency.

The following types of data are available to be imported through VectorSurv's web service import process.

- Surveillance Sites
- Arthropod Collections
- Arthropod Pools
- Sentinel Bands
- Sentinel Band Bleeds

The import process for VectorSurv's web service can also be tested in the VectorSurv Sandbox (<https://sandbox.vectorsurv.org/>). As with all data entered to the VectorSurv Sandbox, data imported to the VectorSurv Sandbox do not persist, as the Sandbox is reset each weekend.

Assistance with VectorSurv's web service import process can also be provided by VectorSurv's staff when available. Please reach out to VectorSurv at ![Help Email] to request such assistance.

[Return to Top](#TableOfContents)

## Exporting Data from VectorSurv {#ExportingData}

In addition to viewing data through the VectorSurv Gateway user interface, VectorSurv allows for previously entered data of various types to be exported to external files, such as CSV (.csv), Excel (.xls), and JSON (.json) files. Data can be exported from VectorSurv in two separate ways.

**Excel (.xls) or CSV (.csv) File Exports:**

Previously entered data of various types within VectorSurv can be exported through the use of the VectorSurv Gateway's export process. Users can export files from VectorSurv by navigating to [Tools] > [Data Tools] > [Export Data].

The following types of data are available to be exported to Excel (.xls) or CSV (.csv) files through the VectorSurv Gateway's export process.

- Surveillance Sites
- Arthropod Collections
- Arthropod Collections (with species and gender structured in a spreadsheet-style format)
- Arthropod Pools
- Arthropod Pool Test Results
- Sentinel Bands
- Sentinel Band Bleeds
- Sentinel Band Bleed Test Results
- Pesticide Application
- Application Technicians
- Application Mixes
- Application Equipment
- Application Source
- Tick Collections
- Tick Collections (with species and gender structured in a spreadsheet-style format)
- Tick Pools
- Carcass Reports
- Carcass Submissions
- Carcass Submission Test Results

The export process to Excel (.xls) or CSV (.csv) files can also be tested in the VectorSurv Sandbox (<https://sandbox.vectorsurv.org/>).

Assistance with the Excel (.xls) or CSV (.csv) file export process can also be provided by VectorSurv's staff when available. Please reach out to VectorSurv at ![Help Email] to request such assistance.

**Web Service Exports:**

Previously entered data of various types within VectorSurv can also be exported through the use of VectorSurv's web service. This service is primarily intended for agencies with local in-house data applications or for agencies implementing custom code. The specifications for the web service export process can be found on our documentation website (<https://trac.vectorsurv.org/gateway/wiki/ExportWebService>).

To begin using VectorSurv's web service export process, an agency token is required to demonstrate that the export request has the proper authentication. Agency tokens can be generated by navigating to [Settings] > [My Agency] > [Agency Tokens]. Software vendors seeking to connect on behalf of a client agency would need to obtain a token from an agency manager at the client agency.

The following types of data are available to be exported through VectorSurv's web service export process.

- Surveillance Sites
- Arthropod Collections
- Arthropod Pools
- Sentinel Bands
- Sentinel Band Bleeds
- Carcass Reports
- Carcass Submissions
- Carcass Submission Test Results

The export process for VectorSurv's web service can also be tested in the VectorSurv Sandbox (<https://sandbox.vectorsurv.org/>).

Assistance with VectorSurv's web service export process can also be provided by VectorSurv's staff when available. Please reach out to VectorSurv at ![Help Email] to request such assistance.

[Return to Top](#TableOfContents)

## Data Access on VectorSurv {#DataAccess}

**Intra-Agency Data Access:**

VectorSurv's structure allows for agencies and agency managers to determine who is allowed to have access to their agency's data. Agency managers are able to add or remove users from their agency and change user login type (View-only, User, Agency Manager, etc.) by navigating to [Settings] > [My Agency] > [Manage Users].

**Inter-Agency Data Access:**

In addition to a user having access to their own agency's data, users may also request access to log in as a particular type of user for another agency. These login requests can allow the requester of such privileges to become a user, an agency manager, or to have view-only permissions to the requested agency's VectorSurv data. These requests are to be reviewed by an agency manager of the agency for which access has been requested, and the agency receiving the request will determine if the request will be granted or denied. Agency access requests can be submitted by navigating to [Settings] > [My Account] > [Other Agency Access].

**Aggregate Agency Data Access:**

Aggregate agencies are agencies that are responsible for statewide coordination and reporting of vector surveillance and control data. Because of these duties, aggregate agencies have access to VectorSurv data for their entire state. Aggregate agencies typically include statewide public health agencies and central laboratories performing pathogen testing for many local agencies. Aggregate agencies are granted relevant data permissions to all local agencies within their jurisdiction to facilitate statewide data reporting and the organization and dissemination of specimens to be tested and their test results.

**Public Data Sharing:**

When and where data are available, VectorSurv publishes a public data visualization website that presents informative but simplified views of the data stored within the VectorSurv Gateway (<https://maps.vectorsurv.org/>). This website contains pages that are available to all visitors, such as maps showing arbovirus-positive environmental samples, invasive mosquito monitoring, and dengue / Zika virus risk indexes. Also, other beta sites that are available only to visitors who have login privileges for the VectorSurv Gateway. These password-protected maps show vector abundance by agency, pesticide resistance, and West Nile virus risk indexes. These pages serve an important function, as they allow for the timely reporting of relevant data elements to the communities where this data is being collected.

Publicly shared data elements are geospatially obscured in two different ways to provide data privacy for the agencies that generate the underlying data.

The first obscuring technique is to present data aggregated at the level of the represented city, county, or the submitting agency's spatial boundaries. This technique can be seen in the invasive species monitoring and the dengue / Zika risk indexes pages. Presenting aggregated data provides data privacy as these pages do not reveal the actual or relative locations of where the data element represented was collected.

The second obscuring technique is to offset coordinate data values randomly by up to a quarter of a mile. This technique can be seen in the arbovirus positive environmental samples page. Presenting offset coordinate data preserves the overall spatial pattern of arbovirus activity without revealing the actual location of where the data element represented was collected.

**California Data Policy**

For California VectorSurv users, an existing data policy statement (<https://vectorsurv.org/assets/files/calsurv_data_policy.pdf>) outlines permission to use electronically-stored vectorborne disease surveillance data for multiple uses and by various organizations. These guidelines are intended for agencies
that participate in the California Vectorborne Disease Surveillance Program (CalSurv), a joint activity of the Mosquito and Vector Control Association of California (MVCAC), the California Department of Public Health (CDPH), and the University of California, Davis (UCD). This policy is administered by the CalSurv Steering Committee, composed of members from the three agencies listed above.

In addition to the data request form found within the data policy statement, an online data request form is available from the VectorSurv website (<https://vectorsurv.org/>).

[Return to Top](#TableOfContents)

## VectorSurv Citation {#VectorSurvCitation}

It is encouraged that VectorSurv be cited in situations where data stored within VectorSurv are directly used within research papers or journal articles. In general, a citation for the main VectorSurv website is appropriate as it serves as an informational front page for VectorSurv that is more useful for understanding the system. The VectorSurv website is used rather than the VectorSurv Gateway because the Gateway is specifically used by public health and vector control agencies with login credentials. Providing the URL for the VectorSurv Gateway only brings readers to the VectorSurv Gateway login page.

Additionally, for California VectorSurv users, an existing data policy (<https://vectorsurv.org/assets/files/calsurv_data_policy.pdf>) and data request/review process outline the process by which California VectorSurv data can be provided to external researchers or requestees. Therefore, for California-specific research papers or journal articles, an additional statement can be provided as the data availability statement that is frequently required by academic journals.

**VectorSurv Citation:**

VectorSurv Development Team. 20XX. VectorSurv - Vectorborne Disease Surveillance System. URL: https://vectorsurv.org/ [accessed XX Jan-Dec 20XX].

**Data Availability Statement for California VectorSurv Users:**

Mosquito surveillance data can be requested for specific research purposes by submitting a request with details of the proposed project via VectorSurv [https://vectorsurv.org].

[Return to Top](#TableOfContents)

[Settings]: https://gateway.vectorsurv.org/core/ppf/menu/path/3
[My Account]: https://gateway.vectorsurv.org/core/ppf/menu/path/4
[My Agency]: https://gateway.vectorsurv.org/core/ppf/menu/path/5
[Manage Users]: https://gateway.vectorsurv.org/core/ppf/users
[Add New User]: https://gateway.vectorsurv.org/core/ppf/users#new_user_legend
[Account Preferences]: https://gateway.vectorsurv.org/core/ppf/preference
[Manage Users]: https://gateway.vectorsurv.org/core/ppf/users
[Security Details]: https://gateway.vectorsurv.org/core/ppf/password
[Tools]: https://gateway.vectorsurv.org/core/ppf/menu/path/57
[Data Tools]: https://gateway.vectorsurv.org/core/ppf/menu/path/81
[Data Import]: https://gateway.vectorsurv.org/core/ppf/import
[Agency Tokens]: https://gateway.vectorsurv.org/core/ppf/token_agency
[Export Data]: https://gateway.vectorsurv.org/core/ppf/export
[Other Agency Access]: https://gateway.vectorsurv.org/core/ppf/agency_access
[Help Email]: {{starting}}/assets/images/docs/help_email.png

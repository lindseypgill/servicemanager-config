# Intelligent Capture Designer
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/configuration/intelligent-capture/intelligent-capture-designer.md]]

## Global Variables
Global variables are available throughout the Intelligent Capture workflow. These will allow branching to be used based on these values

* **Portal Type**<br>This global variable lets you determine the branching based on one of two entry points. This could either be from one of the customer portals (Portals) or the main Hornbill client (Service Desk).

* **Source**<br>This global variable lets you determine the branching of an Intelligent Capture script based on the pro.vided sources. The options for source include Analyst, Chat, Email, Post, Request, Self Service

Personalize Intelligent Capture forms based on the logged in user. The variables listed below can be used within the Custom Forms on the Form Prompt, Field Labels, and Field Descriptions. Each variable is placed within a double set of curly brackets. For example {{user.fName}}

* **user.fName**<br>Dislpays the first name of the logged in user.
* **user.lName**<br>Displays the last name of the logged in user.
* **user.accountRefUrn**<br>Displays the URN ID of the logged in user.
* **user.currentTimeZoneOffset**<br>Displays the current time based on the user's time zone setting.
* **user.userId**<br>Displays the User ID of the logged in user.
* **user.userName**<br>Displays the full name (first and last) of the logged in user.
* **user.jobTitle**<br>Displays the job title of the logged in user.
* **user.mobile**<br>Displays the mobile phone number of the logged in user.
* **user.email**<br>Displays the email of the logged in user.
* **user.phone**<br>Displays the work phone number of the logged in user.
* **user.managerName**<br>Displays the name of the manager of the person raising the request.
* **user.siteName**<br>Displays the name of the user's site as set on their profile.
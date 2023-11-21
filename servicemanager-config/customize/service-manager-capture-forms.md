---
layout: article-toc
---
# Service Manager Forms
Service Manager provides a number of default forms that are available to use when building the Intelligent Capture scripts for raising requests. These forms can be made available to an intelligent capture script by adding a form node to your intelligent capture and selecting the form name from within the properties of the node.

### Add Attachments
The 'Add Attachments' form allows you to include files when raising a request. Multiple attachments can be added and individual descriptions can be applied to each. 
* Add attachments such as screen shots while raising a request
* Browse local file system or drag and drop file
* Includes description of attachment for easy reference
* Stores attachments in the Attachments section of a request for easy access
* Option to specify a custom title on the form
* Option to specify a custom information message to describe to the user the type of attachment that you are requesting. This option can contain wiki formatting for improved presentation.

:::tip
Attachments are regulated by the following system settings that restrict size and type:
* maxfileUploadSize
* security.fileUploadRestriction.webdav.enable
* security.fileUploadRestriction.entity.fileAttachments.types
:::

:::tip
More than one attachment form can be included within a single Intelligent Capture workflow. Any subsequent Attachment Form needs to be set to mandatory in order for the Intelligent Capture to stop and prompt the user on that form.
:::

### Assignment
The Assignment form provides options for assigning the request to a team and an owner. You can choose to assign the request to just a team or to a team and a specified owner.
* Search for Team and Owner to assign request
* When preceded by the Service Details Form, only teams that support that service will be displayed
* Only visible to service desk users
* Branch nodes that follow this will be able to use Team Name, Team ID, Anaylst Name, and Analyst ID as criteria for branching

#### Options
* **Owner is manadatory**<br>When set to Yes the owner or analyst field becomes mandatory and must be selected to continue 

### Asset Details
The Asset Details form allows an analyst or customer to associate assets to a request. By default, all assets that are associated to the customer are shown however it is also possible to associate assts which are shared with the customer, or perform general searches on assets that reside at the customer site, or more widely in the system. It's possible to associate multiple assets to each request.

* View Asserts owned and user directly by a customer
* View Assets shared with a customer (directly or via their membership to groups or organizations the asset has been shared with)
* Search assets by site or more widely
* Input: Following a Search Co-worker / Contact or Customer form the assets belonging to or shared with the customer will be displayed
* Visibility: Analysts and Customers
* Branch Options: None
* If this node is preceded by the Sites node, the Sites Tab will be automatically filtered to only display assets located at the selected site.

#### Options
* **Asset Title**<br>Displays a title at the top of the Asset form
* **Info Message**<br>Add a longer descriptive message explaining to the user how to use the form
* **Hide Customer's Assets**<br>Select Yes to always have this tab hidden
* **Hide Shared Assets**<br>Select Yes to always have this tab hidden
* **Hide Customer's Site Assets**<br>Select Yes to always have this tab hidden
* **Hide Company Assets**<br>Select Yes to always have this tab hidden
* **Hide All Assets**<br>Select Yes to always have this tab hidden
* **Hide Service Assets**<br>Select Yes to always have this tab hidden
* **Select Asset Class**<br>On the Asset Search, set the Asset Class to be searched
* **Select Asset Type**<br>On the Asset Search, set the Asset Type to be searched
* **Select Asset Status**<br>On the Asset Search, set the Asset Status to be searched
* **Select Asset Relationship**<br>Specify the default asset relationship which will be the focus of the asset search
* **Asset Search Term**<br>On the Asset Search, set a default Search Term to be searched
* **Select Asset Search Type**<br>On the Asset Search, set if the results return assets with an exact match, contains, or begins with the specified Search Term

:::note
The "Select Asset ..." parameters only affect tabs that search for assets. The Customer's Assets and Shared Assets tabs will show all Assets that are Owned By or Shared With the Customer respectively.
:::

## Change Type
The 'Change Type' form allows an analyst to select the type of change request that will be raised. This form is usually only seen on the new Change capture flow:
* **Select Change Type**

## Connections
The Connections form allows the support person to select a connected customer at the time of raising the request. This form is only used by and visible to support staff when raising the request in Service Manager when using the full client.
* **Connection Search**<br>Search for one or more customers that you would like to add as a connection to the request.
* **Connection Type**<br>A pick list of available Connection Types is available to allow you to select the type of connection being added.

## Customer Search
The 'Customer Search' form allows an analyst to select a customer for the request. This search returns both Contacts and Co-workers. This form is useful when the a support team is supporting both external and internal customers.

* Search on both Contacts and Co-workers
* Filter on Contacts or Co-workers
* The Customers active Requests are displayed when a customer is selected.
    * The list of the customer's Requests can be filtered to only show those which the logging agent supports via the linked service: app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests. When disabled, an agent will have visibility to unsupported customer Requests, this must be avoided for customers with multiple service desks (e.g. IT and HR).
    * An option to add a new Contact can be displayed on this form if the following system setting is enabled: app.itsm.progressiveCapture.customerSearch.allowAddContact
* Advanced filtering
    * By appending one or more of the following keys you can narrow the search to specific areas:
        * org: - this filters by Organization
        * site: - this filters by Site
        * type: - this filters by Co-Worker Type
        * tel: - this filters by the primary telephone number
        * phone: - this is a synonym for tel:
Example:
Joe org: ACME
would return all customers named Joe from the ACME Organization
* Additional Display Fields<br>These can be used to display selected fields within the right-hand side of the Inteligent Capture during the capture process. When one or more fields are added, the default fields will no longer be displayed.  If this option is left blank the following default fields will be displayed
    * Job Title
    * Phone
    * E-mail
    * Mobile
    * Feedback

## Contact Search
The 'Contact Search' form provides a search option for adding a contact as the customer for the request. The search results only displays contact records and is recommended to use when only providing external support.
Search all contacts
Configure fields to be displayed on the right hand side
The Contacts active Requests are displayed when a contact is resolved.
The list of the contact's Requests can be filtered to only show those which the logging agent supports via the linked service: app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests. When disabled, an agent will have visibility to unsupported customer Requests, this must be avoided for customers with multiple service desks (e.g. IT and HR).
An option to add a new Contact can be displayed on this form if the following system setting is enabled: app.itsm.progressiveCapture.contactSearch.allowAddContact

## Co-worker Search
The 'Co-worker Search' form provides a search option for adding a Co-worker as the customer for the request. This search results only displays co-worker records and is recommended to use when only providing internal support.
Search all Co-workers
Configurable field to be displayed on the right hand side
The Co-workers active Requests are displayed when a co-worker is resolved.
The list of the Co-worker's Requests can be filtered to only show those which the logging agent supports via the linked service: app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests. When disabled, an agent will have visibility to unsupported customer Requests, this must be avoided for customers with multiple service desks (e.g. IT and HR).

:::tip
The Co-worker Search includes an additional option to show archived users in the list that is presented to the user.  This can be useful when raising requests regarding people that may have left the company.  
:::

## Known Error Details 
The 'Known Error Details' form allows an analyst to specify root cause and workaround details for a known error. This form is usually only seen on the new Known Error Intelligent Capture script:
Provide root cause and workaround details

## Organization Details
The 'Organization Details' form allows an analyst to see additional information about the customer's organization that is defined by a Hornbill administrator. There is no data captured in this PCF - it is purely informational only.
Display only
Will display the organization of a previously selected contact
Recommended use after the Contact Search
Configurable organization fields for the right hand side

## Release Type
The 'Release Type' form allows an analyst to select the type of release request that will be raised. This form is usually only seen on the new Release Intelligent Capture Script:
Select Release Type

## Request Details
The 'Request Details' form allows an analyst to enter both a summary and a description for the request.
Add summary to the request
Add a detailed description to the request

## Request Priority
The 'Request Priority' form allows the priority of the request to be set.
Select the Priority for the request

## Select Site
The 'Select Site' form allows an analyst or customer to specify a site when logging a request:
The All Sites filter allows you to search for a site by name
If preceded by the customer / co-worker form, this will show the option to pick the site associated to the customer
If a customer belongs to a Company internal organizational group, and that Company also has associated sites, then a Company site filter will appear and you can search for sites which are associated to the customers company.
If preceded by the asset form, will show the option to pick the site associated to any of the assets
Branch Options: The name of the selected site can be used in a branch node
Options

Limit Portal Search to Name
If set to No the post code and site ID are included in the search. If set to Yes then only the name of the site name is searched on.
Info Message
Add a longer descriptive message explaining to the user how to use the form
Hide Customer's Site
Select Yes to always have this tab hidden
Hide Company Sites
Select Yes to always have this tab hidden
Hide Asset Sites
Select Yes to always have this tab hidden
Hide All Sites
Select Yes to always have this tab hidden
Hide All Sites in Portals (if all sites option is not hidden)
Select Yes to always have the sites tab hidden when viewing on the portals

## Services
The Services form allows Service Manager user to select a service when capturing information during request creation.  Each service will also display their assocaited request catalog if available.

:::tip
This form will not be displayed to anyone raising requests through the Customer or Employee portals.
:::

### Form Features
* Filter services by name
* Displays Request Catalog under each Service
* If this form is preceded by the Customer, Co-worker, or Contact Search the Service Details will only show the subscribed services for the selected person
* If this form is preceded by the Request Type form, only the Request Catalog Items that match that type will be displayed
* Filter option by Service Category

### Branch Options
The name of the selected service can be used in a branch node

### Application Settings
The following settings can be use to change the behavior of the Services form.  These settings can be updated in the [Application Settings](/servicemanager-config/advanced-tools-and-settings/application-settings) for Service Manager.
|Name|Description|
|-|-|
|servicemanager.progressiveCapture.servicedetails.enableSupportVisibility|Restricts the view so that the list of services also only includes the services supported by the analyst.|
|servicemanager.progressiveCapture.servicedetails.catalogRequired|Enforces the selection of a request catalog item if one exists under a service.|


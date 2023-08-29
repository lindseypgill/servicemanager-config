---
layout: article-toc
---
# Routing Rule Templates
The Routing Rule Templates provide a way to define default settings for requests that are automatically raised from emails using the Email Routing Rules. An unlimited number of Routing Rule Templates can be created. Each Email Routing Rule can link to a single Routing Rule Template. A single Routing Rule Template can be used by multiple Email Routing Rules.

## Template Options

Each Template provides a number of options to define the default settings for the requests that are raised from an email routing rule.

* **Name**<br>The Name is used for both providing a reference in the list of Routing Rule Templates and for selecting the routing rule template when defining a Email Routing Rule when the raiseNewRequest operation is used.
* **Description**<br>An optional description of the Routing Rule Template can be provided to help others that have access to this list understand the purpose of the template.
* **Request Type**,<br>Available request types include Incident and Service Request. This is a mandatory option. The selected option will result in that type of request being raised.
* **Service**<br>All the defined services that have a status of Catalog are available within this list. Despite this being an optional field, using Services is highly recommended.
* **Catalog Item**<br>The Catalog Item option is only available if a service has been selected and that service has available Request Catalog Items
* **Team**<br>Select a Team that this request will be assigned to. Keep in mind that a BPM Workflow can also be used for automating the Team assignments. If a Service has not been selected, all teams will be available to select from. If a service has been selected in the Service field, only the teams that support that Service will be available.
* **Priority**<br>Allows for the initial priority to be set for the request. Keep in mind that the a BPM Workflow can also be used for automating the Priority.
* **Assets**<br>One or more assets can be selected. These assets will be associated to the request and available within the Assets section of the request.
* **Add Attachments**<br>This option determines whether attachments sent on an incoming email are added to the request as attachments for display within the request's 'Attachments' section.

## Routing Rule Operations
Service Manager provides a number of Routing Rule Operations that can be selected when configuring the system Email Routing Rules. The Routing Rule Templates are only available to the raiseNewRequest operation.

* **raiseNewRequest**<br>This operation must be used if you wish to use the Routing Rule Templates. When this operation is selected on an Email Routing Rule, an option is made available to select the Routing Rule Template that you wish to use when that Email Routing Rule is met.
* **updateRequest**<br>This operation does not use Routing Rule templates. This uses the default application settings to set the requests' initial settings
* **logOrUpdateIncident**<br>This operation does not use Routing Rule templates. This uses the default application settings to set the requests' initial settings
* **logOrUpdateRequest**<br>This operation does not use Routing Rule templates. This uses the default application settings to set the requests' initial settings

## Attachments
Attachments can be automatically added to the request attachments section using the following operations.

* **raiseNewRequest**<br>When this operation is selected on an Email Routing Rule, the option to enable/disable the adding of attachments is available on the Routing Rule Template that you wish to use when that Email Routing Rule is met.
* **updateRequest**<br>This operation does not use Routing Rule templates. This uses four application settings to control the adding of attachments for Incidents, Service Requests, Changes and Problem Records
    * `app.email.routing.rules.update.addAttachments.IN`
    * `app.email.routing.rules.update.addAttachments.SR`
    * `app.email.routing.rules.update.addAttachments.CH`
    * `app.email.routing.rules.update.addAttachments.PM`

  
<!-- https://wiki.hornbill.com/index.php?title=Routing_Rule_Templates -->
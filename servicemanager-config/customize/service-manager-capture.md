---
layout: article-toc
---
# Using Intelligent Capture
Intelligent Capture allows you to configure what information is collected or captured when a request is being manually raised. This may consist of a single question or a collection of questions that are presented to a user. The captured information can help with the fulfillment of the request.  

![Capture Question](_books/servicemanager-config/customize/images/portal-custom-capture-question.png)
## Topics Covered
* Where Intelligent Capture scripts are used.
* Advanced settings.

## Before You Begin
* Know how to search for settings in [Configuration](/esp-config/getting-started/using-configuration)

## Raising a Request
Intelligent Capture scripts are initiated from the different locations where a new request can be raised. This might be a support person raising a new request from their request list or a customer raising a request on a self service portal.

### Request List
The `Raise New` option located at the top right of the [Request List](/servicemanager-user-guide/request-list/overview/) is split into two functional areas.

![Raise New Request](_books/servicemanager-config/customize/images/raise-new-request-button.png)

* **Raise New**<br>Clicking on the main button labeled `Raise New` will initiate the Intelligent Capture specified in the *app.itsm.progressiveCapture.newRequest* setting. This can be used when the request type is not known when initiating the capture process. The capture script should contain questions that lead the user to be able to select the correct request type. 
* **Request Types**<br>Clicking on the arrow shows a list of available request types that the user has the right to raise.  The Intelligent Capture for each request type can be specified using the associated setting:
    * **New Incident**<br>app.itsm.progressiveCapture.newIncident
    * **New Service Request**<br>app.itsm.progressiveCapture.newServiceRequest
    * **New Problem**<br>app.itsm.progressiveCapture.newProblem
    * **New Known Error**<br>app.itsm.progressiveCapture.newKnownError
    * **New Change**<br>app.itsm.progressiveCapture.newChange
    * **New Release**<br>app.itsm.progressiveCapture.newRelease

The `Raise New` button can also be configured to only show one of the above options. This can be helpful in reducing the overhead of managing multiple Intelligent Capture scripts.
* **Hide**<br>Turn the setting *app.request.raiseNew.hide* to `ON` to hide the generic `Raise New` option and always have the user select a specific request type. Individual Intelligent Captures can be managed for each request type and remove the need to manage a generic Intelligent Capture script for the `Raise New` option.
* **Limit**<br>Turn the setting *app.request.raiseNew.limit* to `ON` to only allow the `Raise New` option and remove the ability for a user to select a specific request type. This removes the need to manage multiple Intelligent Capture scripts per request type. The request type can be determined by using the [Request Type form](/service-manager-config/customize/service-manager-capture-forms#release-type) or by selecting a Request Catalog Item on the [Services form](/service-manager-config/customize/service-manager-capture-forms#services).  

### Email
From the Email View, a new request can be manually raised from an email. Clicking on `Raise Request` from the `More` options button will by default initiate the Intelligent Capture specified in the *app.itsm.progressiveCapture.newRequest* setting. This is the same capture used by the `Raise New` button on the request list.

![Raise Request](_books/servicemanager-config/customize/images/raise-request-from-email.png/)
:::tip
If an alternative capture script is required when raising requests from an email, the setting *app.itsm.progressiveCapture.newReqeustFromEmail* can be used to specify the capture script to use.
:::

### Request Catalog
Each service has a reqeust catalog that can include a number of request models.  Each request model can have an associated Intelligent Capture that is used to collect information specific to that request.

![Request Model](_books/servicemanager-config/customize/images/request-model-capture.png/)

* **Employee and Customer Portals**<br>When a request in the request catalog is used from either the Employee or Customer portal, only this capture script will be used to capture information.

* **Request List or EMail**<br>When a request is raised by someone on the service desk using the `Raise New` option on either the request list or from an email,  the capture script on a request model will only be used after selecting that request on the [Services Form](/servicemanager-config/customize/service-manager-capture-forms#services).
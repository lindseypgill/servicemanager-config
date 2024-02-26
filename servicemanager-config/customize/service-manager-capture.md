---
layout: article-toc
---
# Using Intelligent Capture
Intelligent Capture allows you to configure how and what information is collected or captured when a request is being manually raised. This may consist of a single question or a collection of questions that are presented to a user. The captured information can help with the fulfillment of the request.  

![Capture Question](_books/servicemanager-config/customize/images/portal-custom-capture-question.png)
## Topics Covered
* Where Intelligent Capture scripts are used.
* Advanced settings.

## Before You Begin
* Become familiar with the [Intelligent Capture designer](/servicemanager-config/customize/intelligent-capture-designer)
* Know how to search for settings in [Configuration](/esp-config/getting-started/using-configuration)

## Raising a Request
Intelligent Capture scripts are initiated from the different locations where a new request can be raised. This might be a support person raising a new request from their request list or a customer raising a request on a self service portal.

### Request List
The Raise New option located at the top right of the Request List is split into two functional areas.

* **Raise New**<br>Clicking on the main button labeled `Raise New` will initiate the Intelligent Capture specified in the *app.itsm.progressiveCapture.newRequest* setting. This can be used when the request type is not known or the user is unsure which request type to select.
* **Request Types**<br>Clicking on the arrow shows a list of available request types that the user has the right to raise.  The Intelligent Capture for each request type can be specified using the associated setting
    * app.itsm.progressiveCapture.newIncident
    * app.itsm.progressiveCapture.newServiceRequest
    * app.itsm.progressiveCapture.newProblem
    * app.itsm.progressiveCapture.newKnownError
    * app.itsm.progressiveCapture.newChange
    * app.itsm.progressiveCapture.newRelease

The `Raise New` button can also be configured to only show one of the above options. This can be helpful with reducing the overhead of managing multiple Intelligent Capture scripts.
* **Hide**<br>Turn the setting *app.request.raiseNew.hide* to `ON` to hide the generic `Raise New` option and always have the user select a specific request type. Individual Intelligent Captures can be managed for each request type and remove the need to manage a generic Intelligent Capture script for the `Raise New` option.
* **Limit**<br>Turn the setting *app.request.raiseNew.limit* to `ON` to only allow the `Raise New` option and remove the ability for a user to select a specific request type. This completely removes the need to manage multiple Intelligent Capture scripts per request type. The request type can be determined by using the [Request Type form](/service-manager-config/customize/service-manager-capture-forms#release-type) or by selecting a Request Catalog Item on the [Services form](/service-manager-config/customize/service-manager-capture-forms#services).  

### Email
From the Email View, a new request can be manually raised from an email. Clicking on the `Raise New`button will by default initiate the Intelligent Capture specified in the *app.itsm.progressiveCapture.newRequest* setting.

The setting *app.itsm.progressiveCapture.newReqeustFromEmail* setting allow the Intelligent Capture to use a specific script when raising a request from an email.

## Default Settings
Service Manager settings are available to configure the default Intelligent Captures that are used when raising requests.

* **app.itsm.progressiveCapture.newRequest**<br>The named Intelligent Capture on this setting will be used when the `Raise New` option is used.
* **app.itsm.progressiveCapture.newIncident**<br>The named Intelligent Capture on this setting will be used when raising an incident.
* **app.itsm.progressiveCapture.newServiceRequest**<br>The named Intelligent Capture on this setting will be used.
* **app.itsm.progressiveCapture.newProblem**<br>Default when raising problems.
* **app.itsm.progressiveCapture.newKnownError**<br>Default when raising known errors.
* **app.itsm.progressiveCapture.newChange**<br>Default when raising a change
* **app.itsm.progressiveCapture.newRelease**<br>Default when raising a release
* **app.itsm.progressiveCapture.newRequestFromEmail**<br>The name of the Intelligent Capture script to use when raising a request from the `Raise New Request` plug-in located within the email view. The default used when this is not set is the New Request Intelligent Capture.

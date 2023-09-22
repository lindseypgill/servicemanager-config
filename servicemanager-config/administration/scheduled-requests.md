---
layout: article-toc
---
# Scheduled Requests

:::important
Coming soon - this feature will be included in a Service Manager update in the very near future!
:::

The Scheduled Requests feature allows Service Manager requests to be automatically created on a set schedule.  For example, there may be a need to schedule a change to your environment that happens each week or month.


## Adding a Scheduled Request

### Details
* **Name**<br>This is a mandatory field and also has to be unique in name to other scheduled requests.  This field is also used to set the summary field of the request.
* **Description**<br>This information is added to the description field of the scheduled request.
* **Request Type**<br>The available request types for scheduling are Incident, Service Request, and Change. 
    :::tip
    Make sure that the request type you wish to use is enabled and configured on the service that you wish to use.
    :::
* **Service**<br>This field will show the services that the current user supports. Select the Service that the scheduled request will be associated with.
* **Catalog**<br>Select the  request catalog item that will be associated to this request.  
    :::note
    As this is an automated scheduled request, the Intelligent Capture associated to this request catalog item will not be used to capture information.
    :::
* **Team**<br>The team that this request will be assigned to.  Make sure that this team supports the selected service.

### Assets
One or more assets can be associated to the scheduled request.

### Scheduling
#### Recurrence pattern
Select one of the following scheduling options
* Run Once
* Run Daily
* Run Monthly
* Run Every Period

#### Next event date
When first creating a scheduled request, set the date and time for the first event will take place.  Once the first event has happened, this field will display the date and time of the next scheduled event.
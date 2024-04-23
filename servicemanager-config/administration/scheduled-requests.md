---
layout: article-toc
---
# Scheduled Requests
The Scheduled Requests feature enables Service Manager requests to be generated automatically with a predetermined timetable.  For instance, there may be a need to schedule a change to your environment that happens on a weekly or monthly basis.

## Topics Covered
* Accessing Scheduled Requests.
* Creating a scheduled request.
* Re-activate an expired scheduled request.

## Before You Begin
* A user requires either the Service Desk Admin or the Hornbill Admin role.

## Accessing
* Open [Configuration](/esp-config/getting-started/using-configuration) and search for Scheduled Requests.
* Select `Scheduled Requests` from the results list.

-or-

* Open [Configuration](/esp-config/getting-started/using-configuration) and select `Service Manager` from the navigation drop down
* Browse the navigation pain for the **Administration** section.
* Select `Scheduled Requests`

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

#### Expiry Count
All but the **Run Once** option have an expiry count.  This option limits the number of times the scheduled request will run.  Independent of how many days or months are selected in the schedule, the schedule requests will stop once this number has been reached. Use -1 if don't want to limit the number of times that the scheduled request is run.

## Re-Activate an Expired Scheduled Request
After a scheduled request has been completed and there are no more recurrences to create a new request, the status is changed to `Expired`.  If you wish to reuse an expired scheduled request

1. Open the list of Scheduled Requests.
1. Click on the `Update` option on the expired Scheduled Request that needs to be re-activated.
1. Update the schedule and set up a new schedule.
1. Click on the `Re-activate` button.

## Schedule Calendar
A calendar view has been provided as a convieniant way to view schedule requests. For each scheduled request, the initial logged request along with its next scheduled event will be displayed in the calendar. The calendar can be accessed by clicking on the `Schedule Calendar` button.
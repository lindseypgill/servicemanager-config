---
layout: article-toc
---
# Using Business Processes with Service Manager
Business processes are used to drive both manual interactions and automation on a request record.  

## Before You Begin
* Be familiar with how to use the Business Process Workflow Designer
* Know how to use Configuration to change application settings

## Where Business Processes are Used
Business processes can be used on incidents, requests, problems, known errors, changes, and releases. 

There is a hierarchy of where business processes can be set to determine which process is used when a request is raised.

* **Request Catalog Item**<br>This is a request template that is made available on the portals and to the service desk.  A business process can be associated to each request catalog item.  If no process is specified, a default process set on the associated service will be used.
* **Service**<br>A default process can be specified on a service that will apply to all requests that are are created without using a request catalog item or a process has not been specified on the request catalog item.
* **Default Settings**<br>There is a setting for each request type where you can specify which business process is used. By default these are not set. If a request has not been allocated a process by the request catalog item or the service, it will look at these default settings.  If a process is not specified in these settings, the request will be raised without a process.

    |Setting|Description|
    |-|-|   
    |app.requests.defaultBPMProcess.change|The default business process to be used when logging a Change and no process is specified.|
    |app.requests.defaultBPMProcess.incident|The default business process to be used when logging an Incident and no process is specified|
    |app.requests.defaultBPMProcess.knownerror|The default business process to be used when logging a known error and no process is specified.|
    |app.requests.defaultBPMProcess.problem|The default business process to be used when logging a Problem and no process is specified.|
    |app.requests.defaultBPMProcess.release|The default business process to be used when logging a Release and no process is specified.|
    |app.requests.defaultBPMProcess.service|The default business process to be used when logging a Service Request and no process is specified.|

    ## Process Tracker
    The Process Tracker is a graphical representation of the business process that is displayed at the top of a request. This is an optional display which uses stages and checkpoints within a process to visualize the progress. The process tracker will be displayed when:
    * On a single stage process, at least one checkpoint has been set up.
    * There is more than one stage in a process.

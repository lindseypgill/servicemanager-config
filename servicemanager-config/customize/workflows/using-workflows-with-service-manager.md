---
layout: article-toc
---
# Using Workflows with Service Manager
Workflows are used to drive both manual interactions and automation on a request record.  

## Before You Begin
* Be familiar with how to use the Workflow Designer
* Know how to use Configuration to change application settings

## Where Workflows are Used
Workflows can be used on incidents, requests, problems, known errors, changes, and releases. 

There is a hierarchy of where workflows can be set to determine which workflow is used when a request is raised.

* **Request Catalog Item**<br>This is a request template that is made available on the portals and to the service desk.  A workflow can be associated to each request catalog item.  If no workflow is specified, a default workflow set on the associated service will be used.
* **Service**<br>A default workflow can be specified on a service that will apply to all requests that are are created without using a request catalog item or a workflow has not been specified on the request catalog item.
* **Default Settings**<br>There is a setting for each request type where you can specify which workflow is used. By default these are not set. If a request has not been allocated a workflow by the request catalog item or the service, it will look at these default settings.  If a workflow is not specified in these settings, the request will be raised without a workflow.

    |Setting|Description|
    |-|-|   
    |app.requests.defaultBPMProcess.change|The default workflow to be used when logging a Change and no process is specified.|
    |app.requests.defaultBPMProcess.incident|The default workflow to be used when logging an Incident and no process is specified|
    |app.requests.defaultBPMProcess.knownerror|The default workflow to be used when logging a known error and no process is specified.|
    |app.requests.defaultBPMProcess.problem|The default workflow to be used when logging a Problem and no process is specified.|
    |app.requests.defaultBPMProcess.release|The default workflow to be used when logging a Release and no process is specified.|
    |app.requests.defaultBPMProcess.service|The default workflow to be used when logging a Service Request and no process is specified.|

    ## Workflow Tracker
    The Workflow Tracker is a graphical representation of the workflow that is displayed at the top of a request. This is an optional display which uses stages and checkpoints within a workflow to visualize the progress. The workflow tracker will be displayed when:
    * On a single stage workflow, at least one checkpoint has been set up.
    * There is more than one stage in a workflow.

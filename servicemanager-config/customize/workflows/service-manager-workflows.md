---
layout: article-toc
---
# General Request Automation
The Service Manager Workflows are used to automate the processing of the requests that have been raised. This page contains information on the Service Manager automated tasks that can be used in the Workflow Designer to build unique and powerful workflows for your requests.


### Access Control
Use the Access Control to lock or unlock the Details section or the Actions on a request. Only users with the appropriate application right (update locked requests) will be able to modify the details or use an Action once locked. This right has been added to the following roles: Incident Management Full Access, Change Management Full Access, Problem Management Full Access, Release Management Full Access, Service Request Full Access, and Service Desk Admin.

Lock / Unlock Request Actions
Lock Request Details
Unlock Request Details

### Assessment
Use the Assessment node to initiate an Impact Assessment on a request

Impact Assessment
### Assets
Use these Hornbill Automations for managing assets that are associated to the request

Add All Owned by Customer
Add Generic Assets Owned by Customer
Add Computer System Assets Owned by Customer
Add Computer Peripheral Assets Owned by Customer
Add Mobile Device Assets Owned by Customer
Add Network Device Assets Owned by Customer
Add Printer Assets Owned by Customer
Add Software Assets Owned by Customer
Add Telecoms Assets Owned by Customer
Create Generic Asset
Create Computer System Asset
Create Computer Peripheral Asset
Create Mobile Device Asset
Create Network Device Asset
Create Printer Asset
Get All Assets
Get All Generic Assets
Get All Computer Peripheral Assets
Get All Mobile Device Assets
Get All Network Device Assets
Get All Printer Assets
Get All Software Assets
Get All Telecoms Assets
Update All Assets - General Information
Update Computer Assets - Additional Properties
Update Computer Assets - General Information
Update Computer Peripheral Assets - Additional Properties
Update Computer Peripheral Assets - General Information
Update Mobile Device Assets - Additional Properties
Update Mobile Device Assets - General Information
Update Network Device Assets - Additional Properties
Update Network Device Assets - General Information
Update Printer Assets - Additional Properties
Update Printer Assets - General Information
Update Software Assets - Additional Properties
Update Software Assets - General Information
Update Telecoms Assets - General Information

### Assignment
Use the Assignment node to automatically assign a request to different Service Manager users or teams.

Assign to Service Team
Assign to Team
Assign to Owner
Assign to Owner (Variable)
Assign to Request Creator
Assign to Most Available Analyst
Assign on Round Robin Basis

### Authorization Decision
Use the Authorization Decision node to mark on a Change or Service Request form if an authorization decision has been made.

Approved
Rejected
Clear

### Collaboration
Use the Collaboration node to post an automated update onto a public workspace at any stage in a workflow. This will be visible to members of the specified workspace, on the timeline of the workspace and their News Feeds.

Comment on Existing Public Workspace Post
Comment on Request Source Post
Post to Public Workspace

### Email Notifications
Use the Email Notification nodes to send email templates to different Request stakeholders. Configuration options include recipient, which email template to use and which mailbox to send the email from.

Email Contact
Email Co-worker
Email Customer
Email Customer Manager
Email External Address
Email Request Owner

### Get Request Information
Use the Get Request Information node at any stage in a workflow and preceding another workflow node when you want to make the variables of the Request available. Variables may include Customer, Status, Site, Priority, or any Answers to Customer defined questions from different Progressive capture forms or attributes of the customer or organization of the request the workflow is running against.

Category Details
Customer Details
Source Email Details
Organization Details
Owner Details
Request Details
Progressive Capture Answers
Service Details
Site Details
Team Details

### Integration
Use the Integration node at any stage of a workflow, where you wish to invoke specific actions against a 3rd party application from the available list of applications.

Create Jira Request
Add Jira Request Comment
Log New Service Request

### Linked Requests
Use the Linked Requests node to automatically post updates and resolve linked Requests. Linked requests are those that have been linked using the Link Action Item on a request form.

Resolve Linked Requests
Update Linked Requests

### Log Requests
Use the Log Request to automatically raise another request at a particular point in the workflow.

Log New Change
Log New Incident
Log New Known Error
Log New Problem
Log New Release
Log New Request

:::note
Using these options in your workflows, please be aware of where you are invoking them / placing them in the workflow, and in turn which workflows are going to be invoked against the new Incident or Service Request raised. Please avoid scenario's where one workflow may invoke the logging of a new request, where the new request's workflow immediately is configured to log a new request which again has a workflow which again logs another request immediately creating a loop. The result of which may be a lot of unwanted requests. In the event this occurs, disable the causing workflow and resolve the issue.
:::

### Questions
Delete Questions

### Request Service
Use the Request Service node, if you wish to automate the availability status setting of the service associated to a request, or to automate adding related services of the request service to the request.

Add Related Services
Update Service Status

### Suspend
Use the Suspend nodes if you wish to suspend the progress of the workflow until a defined action is performed manually on the Request. This could include waiting for a Priority to be set, a Customer added, Ownership set or the Resolution defined. Configuration options include the ability to specify the context (which Action Bar icon) the Request will appear in whilst waiting for the Suspend (manual action) to be performed.

Await Expiry
Wait for List of Request Authorizers
Wait for Attachment
Wait for Request Closure
Wait for Request Closure Category
Wait for Customer
Wait for Feedback
Wait for Request Description
Wait for Document
Wait for Request Email
Wait for External Reference
Wait for Impact Assessment
Wait for Linked Assets
Wait for Linked Request
Wait for Linked Requests Completion
Wait for Linked Request Update
Wait for Linked Services
Wait for New Request Owner
Wait for Request Off Hold
Wait for Request Owner
Wait for Request Priority
Wait for Request Category
Wait for Request Resolution
Wait for Request Site
Wait for Status Change
Wait for Request Summary
Wait for Request Team
Wait for Request Update

### Update Request
Use the Update Request node to automatically update the values of specific Request attributes at any stage in the workflow. Examples being updating the Logging or Closing Categories of a Request.

Logging Category
Closure Category
Update Customer
Update Custom Fields
Details
External Reference
First Time Fix
Place On Hold
Priority
Resolution Text
Service
Service Level
Site
Site (Customer' Site)
Source
Status / Sub-status
Timeline

### Request Timers
Use the Request Timer nodes at any stage in the workflow to either start or stop the Response and or Resolution timers. It is not a perquisite to have to use any timers within workflows or to have to use both Response and Resolution timers when timers are used.

There are some settings that control the default behavior of the Service Level Timers. The settings provided to pause or stop the resolution timer when resolving a request are as follows:

app.request.pauseResolutionTimerOnResolve (Default OFF)
app.request.resumeResolutionTimerOnReopen (Default OFF)
app.request.stopResolutionTimerOnResolve (Default ON)
app.request.stopResolutionTimerOnClose (Default OFF)

Using settings to control resolution timers
You should choose the relevant settings to meet your needs, but note that app.request.stopResolutionTimerOnResolve will take precedence over app.request.pauseResolutionTimerOnResolve so ensure only the one you want to use is enabled.
Using BPM nodes to control resolution timers
If you are using this BPM node to control resolution timers the four settings above should all be turned off; If any settings are enabled then they will take precedence over BPM actions. To enable pause/resume of a resolved request you can add the Timer > Pause Resolution Timer or Timer > Resume Resolution Timer BPM nodes as required in your workflow.

Start Resolver Timer
Stop Resolution Timer
Start Response Timer
Stop Response Timer
Pause Resolution Timer
Resume Resolution Timer
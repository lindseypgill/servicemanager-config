# First Time Fix
First Time Fix (FTF) refers to the outcome of an incident where a fix or resolution is provided to a customer, usually during that first contact with the customer. There are varying definitions to what a first time fix means or what criteria it falls under. In Service Manager we provide workflow automation that lets you define what your requirements are in order to achieve a first time fix.

Achieving a First Time Fix has a number of benefits for both the customer and the service desk. For the customer, there is nothing more satisfying than reporting an issue and getting an immediate resolution. For the Service Desk, achieving a FTF can mean that minimum resources and time were spent on the issue. The more FTFs, the more satisfaction there is for everyone.

## What's covered
* FTF Criteria
* Adding FTF to a BPM Workflow
* Reporting on FTF

## Criteria
The following criteria can be used to determine if the resolution of an incident is considered a first time fix.

* **No Team Reassignments**<br>The team under which the request was originally raised does not change.
* **No Owner Reassignments**<br>The person that raised the incident is also the person that resolved the incident and at no point has it been assigned to anyone else.
* **No Hold Time**<br>The incident cannot be placed on hold.
* **Max Open Time**<br>The incident must be resolved within this timeframe, calculated from the when the incident was logged, to the resolution or closure.

## BPM Workflow
The only thing needed to start tracking first time fixes is to add the Hornbill BPM Automation for First Time Fix to your workflow. The First Time Fix is a simple flag that is set against an incident record through the use of First Time Fix automation. Provided that the criteria defined in this automation is met, the request will be set as a First Time Fix. The First Time Fix automation is best placed within your workflow at a point where you know that the incident has been resolved.

:::tip
If an incident has been flagged as a first time fix, but was then re-opened either through automation or manually, The FTF is removed and set as not being a FTF
:::

## Reporting
The value of tracking FTF comes out of analysis and reporting. This may be to identify which team member is providing the most FTFs or to identify incidents where FTF wasn't reached to investigate how a FTF may be achieved in the future.

### Request List View
From your Service Desk's request list it is quick and easy to list incidents that have achieved a first time fix, or those that haven't. Using either the Advanced Filter or the option to create a new View, select the Criteria for First Time Fix Achieved, and then select the condition is, is not, or not set, depending on the information that you would like to display. Lists can also be exported to a CSV formatted file.

### Personal Dashboard
Using a saved View, you can create a chart that can be placed on your personal dashboard and shared with others.

### Database
The FTF flag is stored in the h_itsm_requests table in the column h_firsttimefix with the following values.

|Value|Description|
|-|-|
|NULL|If the request has not been assessed for FTF the value will be null|
|1|The value will be set to 1 if the FTF has been achieved|
|0|The vulue will be set to 0 if the FTF was not achieved|
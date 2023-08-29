---
layout: article-toc
---
# Request Notices
Use this Hornbill Automation to add or remove a notice which is displayed at the top of the request.

## Add Notice
Use this Hornbill Automation to add a notice to the top of the request.
Options
Request ID
The Request Id of the request the connection(s) are being removed from. This should be set to Auto
Notice Type
The type of notice (Alert or Information). The default value is "Information".
Notice Text
The text that will be displayed. This has a limit of 255 characters
Notice Visibility
The visibility of the notice (Portals
System Timeline Update
Select if the default system text will be added to the timeline for this action
Manual Timeline Update
Select Yes to override the default System timeline Text, and add your own text which will appear in the timeline update for this action
Timeline Visibility
Choose what level of visibility will be automatically applied to this update. Choosing anything other than Customer will result in the customer not seeing the update in the timeline of their requests on the Service or Customer Portals

## Remove Notice
Use this Hornbill Automation to remove one or all notices on a request
Options
Request ID
The Request Id of the request the connection(s) are being removed from. This should be set to Auto
Notice ID
The ID of the notice that needs removing. This can be taken as a variable from the output of the Hornbill Automation that created the notice
Notice Type
This will remove notices of the selected type. Information or Alert
Notice Text Contains
Remove any notice that contains this text
Notice Source
Remove notices based on the source. Either BPM Workflow or Manually added notices.
Notice Visibility
Remove notices that are set to a particular Visibility. Portals, Service Desk, or Both
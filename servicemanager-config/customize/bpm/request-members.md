---
layout: article-toc
---
# Request Members
Use the Request Members node at any stage in a process to automatically add or remove another analyst or subject matter expert into a Request. Members can be added even if they do not have the rights to view the request type, nor the requests which belong to the team against which the request belongs. The added Member's rights will be elevated just for the specific Request. Members can be notified about being added via Hornbill Notifications, and or email depending on the following Service Manager system setting: guest.app.requests.notification.notificationType.members

## Add Request Member
Use this node to add Service Manager analysts to the request. This option allows you to automatically add additional analysts to the request to assist with the resolution or as interested parties.

Options
Request Id
The Request Id of the request the connection(s) are being removed from. This should be set to Auto
Member
This option can contain the Co-worker to be added as a Request member. If supplied, "Member (From Variable)" option will be ignored.
Member (From Variable)
This option can contain the Co-worker to be added as a Request member. If supplied, "Member (From Variable)" option will be ignored

## Remove Request Member
Use this option to remove members from a request.
Options
Request Id
The Request Id of the request the connection(s) are being removed from. This should be set to Auto
Member
This option can contain the Co-worker to be removed from the Request members. If supplied, "Member (From Variable)" option will be ignored
Member (From Variable)
This option can contain the Id of a Co-worker (h_user_id in h_sys_accounts table). This option should only be supplied if "Member" option is not set
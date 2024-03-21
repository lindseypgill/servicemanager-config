---
layout: article-toc
---
# HAi Automations
## Summarize Request
Using the Requests entity in Hornbill Automations and selecting the Type HAi you will find the Summarise Request task, like the UI for summarizing the request the only difference here is it being triggered frm a workflow, optionaly you can update the timeline and the summary is also returned as a variable for use in the process later on.
<img src="/_books/servicemanager-config/administration/images/hai_automation_summaize.png" alt="Hornbill Ai Summarise Request - Automation" ></img>


## askHAi
Using the Requests entity in Hornbill Automations and selecting the Type HAi you will find the askHai task, this allows fairly open prompts to be used as part of a Hornbill Workflow and the following example uses the initial summary and description of a request and asks for some clarifying questions to be generated if possible. Its important to not directly send this straight to a user in the first instance and validate its output but like with other automations the response is optionaly added to the timeline and is also returned as a variable for use in the process later on.

<img src="/_books/servicemanager-config/administration/images/hai_automation_ask.png" alt="Hornbill Ai askHai - Automation" ></img>
<img src="/_books/servicemanager-config/administration/images/hai_automation_ask_2.png" alt="Hornbill Ai askHai - Automation" ></img>
---
layout: article-toc
---
# Assessments

The Service Manager Assessments provide options for priority, impact and urgency in order to evaluate the importance of a request.

## Impact
The Impact Assessment provides a questionnaire to ascertain the level of impact that a particular request may have.

## Assessments
Assessments are a collection of questions that can be created and presented in the user interface to determine impact levels of a request. Multiple assessments can be created and then each assessment individually used within a BPM workflow and presented to a user at an appropriate time in the process.

### Questions
One or more questions can be created for each assessment. One a question has been created, multiple answers can be defined and will allow the user to select the most suitable answers when running through the assessment.

### Answers
Each Question requires one or more answers. Answers are presented to a user as a list of single select radio buttons, only allowing one answer to be selected per question. Each answer provides a Weight Level. This is a value that will be used at the end of the assessment to determine the Impact Level to be applied. The weight levels for all the selected answers are totaled up and the Thresholds are then used to determine the Impact Level.

* **Answer**<br>Write an answer to the question that you have provided.
* **Weight**<br>Enter a numerical value that will represent the weight level for this answer.
* **Language**<br>Translations into other languages can be provided for each answer.
* **Thresholds**<br>The Thresholds determine which Impact Level is set against a request. This is based on an lower and upper limit for each Impact Level where the numbers are calculated against the total value of all the weighting level of all the answered questions.

### Impact Level
The available Impact Levels that have been defined will be available as part of the Thresholds. Additional Impact Levels can be added from the Impact Level option.
### Lower Limit
The lower limit specifies that this Impact Level will be applied if the total of the weighting from all the answers are above this number but below the upper limit.
### Upper Limit
The upper limit specifies that this Impact Level will be applied if the total of the weighting from all the answers are below this number but above the lower limit.
### Auto-set
Provided that there is more than one answer to one or more questions where a weighting level has been specified, clicking on the Auto-set button will equally divide up the lowest possible limit with the highest possible limit across the different available impact levels. Depending on the number of answers that have been defined with a weight value, the results of an Auto-set may still need to be adjusted so that there is no overlap between Impact Levels.

## Urgency
The ability to apply an urgency level to a request is an optional feature which can be enabled using the ON/OFF toggle switch at the top left of the Urgency form. This is turned off by default. When turned on, this will apply to all requests and request types within Hornbill Service Manager and will be available within the Assessment Action on the requests

### Urgency Levels
By default, 4 Urgency Levels are provided. This includes Low, Medium, High, and Critical. The Urgency Levels tab provides options to delete, add, rename, and provide translations for the available Impact Levels.

On the left side of each Urgency level, an icon is visible that allows you to drag and drop in order to change the order that the Urgency levels are displayed.

:::note
The Urgency assessment does not currently come with the ability to build a questionnaire as do Impact levels. This is a planned feature for a future release.
:::

<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Assessments>
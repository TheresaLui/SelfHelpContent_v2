<properties
	articleId="problemscopingques-dsc.md"
	pageTitle="Azure Automation - State Configuration"
	description="Azure Automation - State Configuration"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599856,32627997,32628000,32628001"
	productPesIds="15607"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# State Configuration (DSC)
---
{
	"resourceRequired": true,
	"title": "State Configuration",
	"fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements":
    [
        {
			"id": "problem_start_time",
			"order": 10,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
        },
        {
			"id": "NodeName",
			"order": 20,
			"controlType": "textbox",
			"displayLabel": "Please provide the computer name of one or more affected machines",
			"required": false
        },
        {
			"id": "problem_description",
			"order": 30,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
			"required": true,
			"useAsAdditionalDetails": true,
            "hints":
            [
                {
					"text": "Include the exact text of any error messages that occur"
				}
			]
		}
	]
}
---

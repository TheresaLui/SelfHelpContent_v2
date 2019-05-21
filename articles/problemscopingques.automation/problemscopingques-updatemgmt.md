<properties
	articleId="problemscopingques-updatemgmt.md"
	pageTitle="Azure Automation - Update Management"
	description="Azure Automation - Update Management"
	authors="zjalexander,summertgu"
	ms.author="zachal,tiag"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599861,32599864,32599868,32615228,32599903,32615227,32599924,32599925,32615229,32615226,32599936,32599937,32633803,32633804"
	productPesIds="15607,14749,15571,15797,16454,16470"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Update Management
---
{
	"resourceRequired": true,
	"title": "Update Management",
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
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
            "hints":
            [
                {
					"text": "Include the exact text of any error messages that occur"
				}
			]
		},
		{
			"id": "learn_more_text",
			"order": 40,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/azure/automation/troubleshoot/update-management'>Learn more</a> about troubleshooting Update Management"
		}
	]
}
---

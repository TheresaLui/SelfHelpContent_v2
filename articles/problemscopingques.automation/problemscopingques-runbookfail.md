<properties
	articleId="problemscopingques-runbookfail.md"
	pageTitle="Azure Automation - Runbook Execution"
	description="Azure Automation - Runbook Execution"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599860,32599923,32599906,32599907,32599908,32599909,32615224,32628014,32628013"
	productPesIds="15607"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Runbook Execution
---
{
	"resourceRequired": true,
	"title": "Runbook failure",
	"fileAttachmentHint": "",
    "formElements": 
    [
        {
			"id": "runbook selection",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Select the runbook that has the problem",
			"watermarkText": "Choose a runbook",
            "dynamicDropdownOptions": 
            {
			    "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Automation/automationAccounts/{resourcename}/runbooks?api-version=2017-05-15-preview",
			    "jTokenPath": "value",
			    "textProperty": "name",
			    "valueProperty": "id",
			    "textPropertyRegex": "[^/]+$"
			},
			"required": true
        }, 
        {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
        }, 
        {
			"id": "previously successful",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Has this runbook successfully run in Azure Automation before?",
            "dropdownOptions": 
        [
            {
                "value": "Yes",
                "text": "Yes, this runbook has successfully run in Azure Automation before"
            }, 
            {
                "value": "No",
                "text": "No, this runbook has never successfully run in Azure Automation"
            }
			],
			"required": false
        }, 
        {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
            "hints": 
            [
                {
					"text": "Issue description."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com//azure/automation/troubleshoot/runbooks'>Learn more</a> about troubleshooting runbooks"
		}
	]
}
---

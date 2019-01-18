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
			    "uri": "/subscriptions/{subscriptionId}/resourceGroups/{rgName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/runbooks?api-version=2017-05-15-preview",
			    "jTokenPath": "value",
			    "textProperty": "name",
			    "valueProperty": "id",
			    "textPropertyRegex": "[^/]+$"
			},
			"required": true
        }, 
        {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
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
			"required": false,
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

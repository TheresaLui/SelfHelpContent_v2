<properties
	articleId="problemscopingques-automation"
	pageTitle="PowerShell, REST API or SDK Issue"
	description="PowerShell, REST API or SDK Issue"
	supportTopicIds="32632394"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15551"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_APIManagement"
/>
# PowerShell, REST API or SDK Issue
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "PowerShell, REST API or SDK Issue",
	"fileAttachmentHint": "Please attach any relevant logs/screenshots",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
		{
			"id": "2",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Are you using the latest version of Az PowerShell module?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
		{
			"id": "problem_description",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
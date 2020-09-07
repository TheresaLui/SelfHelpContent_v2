<properties
	pageTitle="Restoring an Accidently Deleted Domain"
	description="Restoring an Accidently Deleted Domain"
	supportTopicIds="32604404"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16513"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-restore-deleted-domain"
	ownershipId="Compute_AppService"
/>
# Restoring an Accidently Deleted Domain
---
{
	"resourceRequired": false,
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"title": "Restoring an Accidently Deleted Domain",
	"fileAttachmentHint": "Please attach any relevant logs and screenshots",
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
			"controlType": "textbox",
			"displayLabel": "How long has it been since you deleted the domain?",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "3",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Have you tried buying the domain again",
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
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
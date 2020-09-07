<properties
	articleId="problemscopingques-api-error"
	pageTitle="API Management APIs returning Other Errors (400, 500, 503, etc.)"
	description="API Management APIs returning Other Errors (400, 500, 503, etc.)"
	supportTopicIds="32632391"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15551"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_APIManagement"
/>
# API Management APIs returning Other Errors (400, 500, 503, etc.)
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "API Management APIs returning Other Errors (400, 500, 503, etc.)",
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
			"displayLabel": "Have you reviewed diagnostic logs to rule out the possibility of errors being returned by the backend?",
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
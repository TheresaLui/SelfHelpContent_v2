<properties
	pageTitle="Purchasing"
	description="Purchasing"
	supportTopicIds="32604403"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16513"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-purchasing"
/>
# Purchasing
---
{
	"resourceRequired": false,
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"title": "Purchasing",
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
			"displayLabel": "If you are hitting the purchase limit, how many more domains are you trying to purchase?",
			"watermarkText": "...",
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
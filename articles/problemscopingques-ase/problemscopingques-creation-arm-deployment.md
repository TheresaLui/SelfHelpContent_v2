<properties
	articleId="problemscopingques-creation-arm-deployment"
	pageTitle="ARM deployment"
	description="ARM deployment"
	supportTopicIds="32608419"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16533"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Developer Portal down or is not responding
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Cannot sign in to Developer Portal",
	"fileAttachmentHint": "Please attach any relevant logs/screenshots as well as the ARM deployment template",
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
			"displayLabel": "What is name of the ASE?",
			"watermarkText": "...",
			"required": false
		},
{
			"id": "3",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "When did the ASE creation start (date and time with time zone)?",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
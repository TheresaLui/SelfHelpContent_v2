<properties
	pageTitle="Hitting Subscription Limit of Amount of Certificates Purchased"
	description="Hitting Subscription Limit of Amount of Certificates Purchased"
	supportTopicIds="32604393"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16512"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-limit"
	ownershipId="Compute_AppService"
/>
# Hitting Subscription Limit of Amount of Certificates Purchased
---
{
	"resourceRequired": false,
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"title": "Hitting Subscription Limit of Amount of Certificates Purchased",
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
			"displayLabel": "How many more certificates are you trying to purchase?",
			"watermarkText": "...",
			"required": true
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
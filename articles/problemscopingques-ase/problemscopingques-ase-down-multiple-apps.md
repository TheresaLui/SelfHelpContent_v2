<properties
	articleId="problemscopingques-ase-down-multiple-apps"
	pageTitle="Multiple web apps affected"
	description="Multiple web apps affected"
	supportTopicIds="32608428"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16533"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Customize Developer Portal
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Cannot sign in to Developer Portal",
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
			"controlType": "textbox",
			"displayLabel": "What framework is your app using (i.e. ASP.NET, Node, Java, Python etc.)?",
			"watermarkText": "...",
			"required": false
		},
				{
			"id": "3",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Is the issue still occurring? If not, how was the issue resolved (i.e. App or Service Restarted, Scaling etc.)?",
			"watermarkText": "...",
			"required": false
		},
				{
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Is there a specific error you are seeing? Please include the text of the error.",
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
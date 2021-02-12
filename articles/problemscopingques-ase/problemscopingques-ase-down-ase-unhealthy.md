<properties
	articleId="problemscopingques-ase-down-ase-unhealthy"
	pageTitle="ASE marked as Unhealthy or Suspended"
	description="ASE marked as Unhealthy or Suspended"
	supportTopicIds="32608420"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16533"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Cannot sign in to Developer Portal
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
			"displayLabel": "What is the name of the ASE",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "3",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Are you aware of any recent changes to ASE or the environment, including Azure Networking? If so, please describe.",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "4",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Is there a banner at the top of the ASE Overview blade in the Portal that indicates a problem?",
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
<properties
	articleId="problemscopingques-deletion"
	pageTitle="Deletion"
	description="Deletion"
	supportTopicIds="32608411"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16533"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Developer Portal UI issue
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
			"displayLabel": "What is the name of the ASE?",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "3",
			"order": 3,
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
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Is the issue that trying to delete results on an error? If so, please describe the exact error and location where you see it.",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Are you aware of any recent changes to ASE or the environment, including Azure Networking? If so, please describe what and when.",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "6",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Are there any App Service Plans or Web Apps still associated to this ASE?",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "problem_description",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
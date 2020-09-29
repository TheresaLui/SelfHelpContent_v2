<properties
	articleId="problemscopingques-scale-ase-instances"
	pageTitle="Scale ASE Instances"
	description="Scale ASE Instances"
	supportTopicIds="32608417"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16533"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Managed Service Identity (MSI) and KeyVault
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Managed Service Identity (MSI) and KeyVault",
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
			"order": 2	,
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
			"displayLabel": "If the issue is that is taking to long to scale, please specify the date and time (with time zone), when you triggered the scaling operation.",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "5",
			"order":5,
			"controlType": "textbox",
			"displayLabel": "Are you aware of any recent changes to ASE or the environment, including Azure Networking? If so, please describe what and when.",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "problem_description",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
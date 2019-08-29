<properties
	articleId="problemscopingques-MSI-keyvault"
	pageTitle="Managed Service Identity (MSI) and KeyVault"
	description="Managed Service Identity (MSI) and KeyVault"
	supportTopicIds="32632421"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15551"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Managed Service Identity (MSI) and KeyVault
---
{
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
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "If you have certificate renewed, what was the renew time?",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "3",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Do you have KeyVault access policies with secrets and certificates configured?",
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
<properties
	pageTitle="	Importing/Exporting App Service Certificates"
	description="	Importing/Exporting App Service Certificates"
	supportTopicIds="32604395"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16512"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-importing-exporting"
	ownershipId="Compute_AppService"
/>
# Importing/Exporting App Service Certificates
---
{
	"resourceRequired": false,
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"title": "Importing/Exporting App Service Certificates",
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
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "If you're trying to import, please specify the App name:",
			"watermarkText": "...",
			"required": false
		},
		{
			"id": "3",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Are you trying to import or export?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Import",
					"text": "Import"
				}, {
					"value": "Export",
					"text": "Export"
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
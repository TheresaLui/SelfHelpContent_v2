<properties
	articleId="problemscopingques-importing-api-openAPI-WSDL"
	pageTitle="Importing API (OpenAPI, WSDL, WADL)"
	description="Importing API (OpenAPI, WSDL, WADL)"
	supportTopicIds="32632419"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15551"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_APIManagement"
/>
# Importing API (OpenAPI, WSDL, WADL)
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Importing API (OpenAPI, WSDL, WADL)",
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
			"displayLabel": "Have you validated your open API spec file at https://editor.swagger.io/ and fixed all errors? If so please attach the spec file",
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
			"id": "3",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "If WSDL cannot be downloaded from the backend, have you tried to save as file and upload?",
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
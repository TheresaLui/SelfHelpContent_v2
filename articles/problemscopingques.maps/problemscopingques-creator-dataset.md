<properties
	articleId="50264922-5153-4cc3-8409-59fa4feb1fe8"
	pageTitle="Maps Creator Dataset service error"
	description="Creator Dataset service error"
	supportTopicIds="32741860"
	authors="anastasia-ms"
	ms.author="v-stharr"
	selfHelpType="problemScopingQuestions"
	productPesIds="16335"
	cloudEnvironments="public,Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureIot_AzureMaps"
/>
# Maps Creator Dataset service error
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Creator Conversion service Issue",
	"fileAttachmentHint": "Upload your Drawing package",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
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
		},
		{
			"id": "problem_api_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "API name:",
			"watermarkText": "Provide the API name.",
			"required": false,
			"useAsAdditionalDetails": true
		},		
		{
			"id": "problem_api_response",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "API response message",
			"watermarkText": "Provide the API response message.",
			"required": false
		},
		{
			"id": "problem_conversion_id",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Conversion ID",
			"watermarkText": "Provide the conversion ID.",
			"required": false
		}
	]
}
---
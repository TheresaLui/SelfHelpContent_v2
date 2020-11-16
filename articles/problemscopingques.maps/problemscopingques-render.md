<properties
	articleId="3c805ef3-9e8e-4691-82bd-528ca4525556"
	pageTitle="Maps Render service error"
	description="Maps Render service error"
	supportTopicIds="32634418"
	authors="anastasia-ms"
	ms.author="v-stharr"
	selfHelpType="problemScopingQuestions"
	productPesIds="16335"
	cloudEnvironments="public,Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureIot_AzureMaps"
/>
# Maps Render service error
---
{
	"subscriptionRequired": true,
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Maps Render service error",
	"fileAttachmentHint": "Upload sample responses.",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
        {
			"id": "problem_api_name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "API name",
			"watermarkText": "",
			"required": false
		},
		{
			"id": "problem_api_request",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "API request",
			"watermarkText": "Provide your API request. Exclude your subscription key.",
			"required": true
		},
		{
			"id": "problem_api_response",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "API response",
			"watermarkText": "",
			"required": false
		},
		{
			"id": "problem_expected_api_response",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Expected API response",
			"watermarkText": "",
			"required": false
		},
		{
			"id": "problem_description",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any additional sample queries and responses you are seeing.  Include any important details about the expected behavior.",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}
---
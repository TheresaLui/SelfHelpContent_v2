<properties
	articleId="problemscopingques-advisory"
	pageTitle="General guidance and advisory"
	description="Generak guidance and advisory"
	supportTopicIds="32588740"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15791"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# On-Premises Data Gateway
---
{
	"resourceRequired": false,
	"title": "General guidance and Advisory",
	"fileAttachmentHint": "Please provide screenshots showing the error or any relevant files",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": false
		},
		{
			"id": "2",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Please provide one or more Run IDs related to this incident.",
			"watermarkText": "Run IDs...",
			"required": false,
		}, 
		{
			"id": "json",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "If you can’t save or update your definition, please share this JSON code with us.",
			"watermarkText": "JSON code...",
			"required": false,
		},
		{
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": false,
			"useAsAdditionalDetails": true
			
		}
	]
}
---

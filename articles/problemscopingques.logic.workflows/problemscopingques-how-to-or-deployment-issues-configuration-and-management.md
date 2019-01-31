<properties
	articleId="problemscopingques-config-and-management"
	pageTitle="Configuration and management"
	description="Configuration and management"
	supportTopicIds="32588755"
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
	"title": "Configuration & Management",
	"fileAttachmentHint": "Please provide screenshots showing the error or any relevant files",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": false
		},
		{
			"id": "3",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Please provide one or more Run IDs related to this incident.",
			"watermarkText": "Run IDs...",
			"required": false,
		}, 
		{
			"id": "history",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Were you able to set this configuration before to this Logic App without errors?",
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
			"id": "json",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "If you can’t save or update your definition, please share this JSON code with us.",
			"watermarkText": "JSON code...",
			"required": false,
		},
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}
			]
		}
	]
}
---

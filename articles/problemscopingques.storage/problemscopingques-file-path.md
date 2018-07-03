<properties
	pageTitle="Storage File path"
	description="Storage File path scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602759,32602770,32602758"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File path scoping question
---
{
	"resourceRequired": true,
	"title": "Storage File path scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "new_or_recurring_issue",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "New or recurring issue",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "new_issue",
					"text": "New issue"
				}, {
					"value": "recurring_issue",
					"text": "Recurring issue"
				}, {
					"value": "advisory",
					"text": "Advisory"
				}
			],
			"required": false
		}, {
			"id": "file_path",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "File share or file path",
			"watermarkText": "FileShare/FileName",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "Approx date and time of the most recent occurance",
			"required": false
		}, {
			"id": "additional_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
<properties
	pageTitle="Storage Blob Container name and path"
	description="Storage Blob Container name and path scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602725,32602728,32602734,32602735"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage Blob Container name and path scoping question
---
{
	"resourceRequired": true,
	"title": "Storage Blob Container name and path scoping question",
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
			"id": "blob_container",
			"order": 2,
			"controlType": "multiselectdropdown",
			"displayLabel": "Blob Container",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/$ref?api-version=2018-03-28",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id",
					"textPropertyRegex": "[^/]+$"
					},
			"required": false
		}, {
			"id": "blob_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Blob name",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate date and time the issue occured",
			"required": false
		}, {
			"id": "additional_details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
<properties
	pageTitle="Storage Blob Container name and path"
	description="Storage Blob Container name and path scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds=""
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
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-03-01-preview",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id",
					"textPropertyRegex": "[^/]+$"
					},
			"dropdownOptions": [{
					"value": "NoBlobContainer",
					"text": "Not specific to a blob container"
				}
			],
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
			"displayLabel": "Approx date and time of the most recent occurance",
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
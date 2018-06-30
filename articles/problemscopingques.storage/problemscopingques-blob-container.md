<properties
	pageTitle="Storage Blob Container"
	description="Storage Blob Container required scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602725,32602728,32602734,32602735"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Recover deleted Storage Account
---
{
	"resourceRequired": true,
	"title": "Storage Blob Container scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "blob_container",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Blob Container",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/$ref?api-version=2017-09-01",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id",
					"textPropertyRegex": "[^/]+$"
					},
			"dropdownOptions": [{
					"value": "All Blob Containers",
					"text": "All Blob Containers"
				}
			],
			"required": false
		}, {
			"id": "blob_path",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Blob path",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate date and time the issue occured",
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
<properties
	pageTitle="Storage Blob Container required"
	description="Storage Blob Container required scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602730"
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
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Blob Container name",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/$ref?api-version=2017-09-01",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id",
					"textPropertyRegex": "[^/]+$"
					},
			"dropdownOptions": [{
					"value": "Unable to get the list of Blob Container",
					"text": "Unable to get the list of Blob Container"
				}
			],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Date and time that the account was deleted",
			"required": false
		}, {
			"id": "additional_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}, {
			"id": "learn_more_text",
			"order": 5,
			"controlType": "infoblock",
			"content": "You can follow our <a href='https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data'>best practices for protecting your data</a> to ensure that your deleted data will be recoverable in the future."
		}
	]
}
---
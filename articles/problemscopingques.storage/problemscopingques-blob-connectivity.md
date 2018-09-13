<properties
	pageTitle="Connectivity issue on blob"
	description="Connectivity issue on blob scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602725,32602734,32602735"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Blob connectivity issue
---
{
	"resourceRequired": true,
	"title": "Connectivity issue on blob scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate start time of the most recent occurrence",
			"required": true
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
			"id": "blob_path",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Blob Path",
			"watermarkText": "'ContainerName/.../BlobName' if specific to a blob",
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
			"content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> to troubleshoot peformance issues."
		}
	]
}
---
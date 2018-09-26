<properties
	pageTitle="Storage File Sync"
	description="Storage File Sync scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602749,32602755,32602756,32602767,32602769"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File Sync scoping question
---
{
	"resourceRequired": false,
	"title": "Storage File Sync scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "file_sync",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "File Sync resource",
			"watermarkText": "Choose a File Sync",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.StorageSync/storageSyncServices?api-version=2018-04-02",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id",
					"textPropertyRegex": "[^/]+$"
					},
			"DropdownOptions": [{
					"value": "NoFileSync",
					"text": "Not specific to a File Sync"
				}
			],
			"required": true
		}, {
			"id": "additional_details",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
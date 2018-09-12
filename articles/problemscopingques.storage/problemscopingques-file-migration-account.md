<properties
	pageTitle="Storage File migration between Storage Accounts"
	description="Storage File migration between Storage Accounts scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602760"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File migration between Storage Accounts
---
{
	"resourceRequired": false,
	"title": "Storage File migration between Storage Accounts scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "storage_account_from",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Source Storage Account",
			"watermarkText": "From StorageAccountName",
			"required": true
		}, {
			"id": "storage_account_to",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Destination Storage Account",
			"watermarkText": "To StorageAccountName",
			"required": true
		}, {
			"id": "file_share",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Destination File Share",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/fileServices?comp=list",
					"jTokenPath": "value",
					"textProperty": "id",
					"valueProperty": "id",
					"textPropertyRegex": "[^/]+$"
					},
			"dropdownOptions": [{
					"value": "NoFileShare",
					"text": "Not specific to a File Share"
				}
			],
			"required": false
		}, {
			"id": "file_share_or_path",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Destination File Name",
			"watermarkText": "'FileName' of 'FileShare/FileName'",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate start time of the most recent occurrence",
			"required": false
		}, {
			"id": "additional_details",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
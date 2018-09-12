<properties
	pageTitle="Storage File connectivity or performance issue"
	description="Storage File connectivity or performance scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602759,32602770,32602761,32602762"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File connectivity or performance issue
---
{
	"resourceRequired": true,
	"title": "Storage File connectivity or performance scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate start time of the most recent occurrence",
			"required": true
		}, {
			"id": "file_share",
			"order": 2,
			"controlType": "multiselectdropdown",
			"displayLabel": "File Share",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/fileServices/default/$ref?api-version=2017-09-01",
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
			"id": "file_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "File name",
			"watermarkText": "'FileName' of 'FileShare/FileName'",
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
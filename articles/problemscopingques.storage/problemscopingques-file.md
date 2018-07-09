<properties
	pageTitle="Storage File Share"
	description="Storage File Share scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds=""
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File Share scoping question
---
{
	"resourceRequired": true,
	"title": "Storage File Share scoping question",
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
			"id": "file_share",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "File Share name",
			"watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
					"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/fileServices//$ref?api-version=2018-03-28",
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
			"id": "problem_start_date",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate date and time of the most recent occurance",
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
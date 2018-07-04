<properties
	pageTitle="Performance issue on blob"
	description="Performance issue on blob scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602726,32602727"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Blob performance issue
---
{
	"resourceRequired": true,
	"title": "Performance issue on blob scoping question",
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
			"id": "blob_or_container",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Container name or blob path",
			"watermarkText": "Enter details when issue occur on specific blob or container",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "Approx date and time of the most recent occurance",
			"required": false
		}, {
			"id": "request_id",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Request ID",
			"required": false
		}, {
			"id": "additional_details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> to troubleshoot peformance issues."
		}
	]
}
---
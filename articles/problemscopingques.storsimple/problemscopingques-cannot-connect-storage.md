<properties
	articleId="6ff4a427-59b8-40f5-a197-59d7cd7f6623"
	pageTitle="Scoping for cannot connect to storage account"
	description="Cannot connect to storage account scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630495"
	productPesIds="15438"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Cannot connect to storage account
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Cannot connect to storage account",
	"fileAttachmentHint": "",
	"formElements": [{
		"id": "storage account",
		"order": 1,
		"controlType": "textbox",
		"displayLabel": "Name the storage account that is not reachable",
		"watermarkText": "Storage account name",
		"required": false
	}, {
		"id": "serial number",
		"order": 2,
		"controlType": "textbox",
		"displayLabel": "Storage account location",
		"watermarkText": "Eg. EastUS, WestUS, etc.",
		"required": false
	}, {
		"id": "problem_start_time",
		"order": 3,
		"controlType": "datetimepicker",
		"displayLabel": "When did the problem begin?",
		"required": true
	}, {
		"id": "problem_description",
		"order": 4,
		"controlType": "multilinetextbox",
		"displayLabel": "Details",
		"watermarkText": "Provide additional information about your issue",
		"required": true,
		"useAsAdditionalDetails": true
	}]
}
---

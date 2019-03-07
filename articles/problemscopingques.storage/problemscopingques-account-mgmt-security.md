<properties
	pageTitle="Security issue on Account Management"
	description="Security issue on account management scoping question"
	authors="ramMSFT"
	ms.author="raprasad"
	selfHelpType="problemScopingQuestions"
	articleId="StorageScoping_accountManagement_security"
	supportTopicIds="32602691,32602695,32602697"
	productPesIds="15629"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Blob Security Issue
---
{
	"resourceRequired": true,
	"title": "Security issue on blob scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Local start time of the latest occurrence",
			"required": true
		}, {
			"id": "error_code_dropdown",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Error code",
			"watermarkText": "HTTP error of failed operation",
			"dropdownOptions": [{
					"value": "HTTP_304",
					"text": "HTTP 304"
				}, {
					"value": "HTTP_400",
					"text": "HTTP 400"
				}, {
					"value": "HTTP_403",
					"text": "HTTP 403"
				}, {
					"value": "HTTP_404",
					"text": "HTTP 404"
				}, {
					"value": "HTTP_405",
					"text": "HTTP 405"
				}, {
					"value": "HTTP_409",
					"text": "HTTP 409"
				}, {
					"value": "HTTP_411",
					"text": "HTTP 411"
				}, {
					"value": "HTTP_412",
					"text": "HTTP 412"
				}, {
					"value": "HTTP_413",
					"text": "HTTP 413"
				}, {
					"value": "HTTP_415",
					"text": "HTTP 415"
				}, {
					"value": "HTTP_416",
					"text": "HTTP 416"
				}, {
					"value": "HTTP_500",
					"text": "HTTP 500"
				}, {
					"value": "HTTP_501",
					"text": "HTTP 501"
				}, {
					"value": "HTTP_502",
					"text": "HTTP 502"
				}, {
					"value": "HTTP_503",
					"text": "HTTP 503"
				}, {
					"value": "other",
					"text": "Not listed above  "
				}
			],
			"required": false
		}, {
			"id": "request_id",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Storage server Request ID",
			"watermarkText": "Request ID of failed operation ending with 000000",
			"textPropertyRegex":"^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
			"required": false
        }, {
			"id": "problem_description",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": true,
			"useAsAdditionalDetails": true
		}, {
			"id": "learn_more_text",
			"order": 7,
			"controlType": "infoblock",
			"content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> performance issues."
		}
	]
}
---

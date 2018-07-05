<properties
	pageTitle="Performance issue on blob"
	description="Performance issue on blob scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602726,32602727,32602725,32602734,32602735"
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
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate start time of the most recent occurrence",
			"required": true
		}, {
			"id": "blob_or_container",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Container name or Blob path",
			"watermarkText": "'ContainerName' or 'ContainerName/BlobName' if specific to a container or blob",
			"required": false
		}, {
			"id": "request_id",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "<a href='https://docs.microsoft.com/rest/api/storageservices/troubleshooting-api-operations#Thex-ms-request-idheader'>Server request ID</a> of the most recent occurrence",
			"watermarkText":"Server request ID",
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
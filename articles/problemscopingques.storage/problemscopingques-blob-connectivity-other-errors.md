<properties
	pageTitle="Blob connectivity other blob service errors"
	description="Blob connectivity and other blob service errors scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602728"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Blob connectivity other blob service errors
---
{
	"resourceRequired": true,
	"title": "Blob connectivity other blob service errors scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate start time of the most recent occurrence",
			"required": true
		}, {
			"id": "error_code_message",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Error code and/or message",
			"watermarkText": "Error code: error message",
			"required": false
		}, {
			"id": "blob_or_container",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Container name or Blob path",
			"watermarkText": "'ContainerName' or 'ContainerName/BlobName' if specific to a container or blob",
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

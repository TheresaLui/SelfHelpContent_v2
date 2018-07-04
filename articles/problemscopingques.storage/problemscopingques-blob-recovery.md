<properties
	pageTitle="Storage Blob recovery"
	description="Storage Blob recovery scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608637"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Recover deleted Blob
---
{
	"resourceRequired": true,
	"title": "Storage Blob recovery scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "blob_path",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Path of Blob to recover",
			"watermarkText": "ContainerName/BlobName",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate date and time the Blob was deleted",
			"required": false
		}, {
			"id": "additional_details",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
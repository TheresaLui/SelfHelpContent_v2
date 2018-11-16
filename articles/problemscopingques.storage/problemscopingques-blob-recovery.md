<properties
	pageTitle="Storage Blob recovery"
	description="Storage Blob recovery scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608638"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Recover deleted Blob
---
{
	"resourceRequired": false,
	"title": "Storage Blob recovery scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate time Blob was deleted",
			"required": false
		}, {
			"id": "blob_path",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Blob path",
			"watermarkText": "'ContainerName/.../BlobName'",
			"required": false
		}, {
			"id": "problem_description",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
<properties
	pageTitle="Unable to delete Blob or Container"
	description="Unable to delete Blob or Container scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602738"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Unable to delete Blob or Container
---
{
	"resourceRequired": true,
	"title": "Unable to delete Blob or Container scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "blob_path_or_container_name",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Container name or blob path",
			"watermarkText": "'ContainerName' or 'ContainerName/BlobName'",
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Approximate date and time of the latest deletion attempt",
			"required": false
		}, {
			"id": "additional_details",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}, {
			"id": "learn_more_text",
			"order": 4,
			"controlType": "infoblock",
			"content": "Please ensure that there is no lease or <a href='https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors'>VM attached to the blob or container</a> you are trying to delete."
		}
	]
}
---
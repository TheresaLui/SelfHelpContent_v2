<properties
	pageTitle="Storage Blob Container recovery"
	description="Storage Blob Container recovery scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602730"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Recover deleted Storage Account
---
{
	"resourceRequired": true,
	"title": "Storage Blob Container recovery scoping question",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "blob_container",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Blob Container name",
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Date and time the Blob Container was deleted",
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
			"content": "You can follow our <a href='https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data'>best practices for protecting your data</a> to ensure that your deleted data will be recoverable in the future."
		}
	]
}
---
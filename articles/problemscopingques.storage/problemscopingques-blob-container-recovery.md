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
# Recover deleted Blob Container
---
{
    "resourceRequired": true,
    "title": "Storage Blob Container recovery scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "warning_same_name",
            "order": 1,
            "controlType": "infoblock",
            "content": "WARNING: Do not recreate Container with the same name while we attempt to recover it."
        },
        {
            "id": "blob_container",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Name of Container to recover",
            "watermarkText": "ContainerName",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time the Container was deleted",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 5,
            "controlType": "infoblock",
            "content": "You can follow our <a href='https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data'>best practices for protecting your data</a> to ensure that your deleted data will be recoverable in the future."
        }
    ]
}
---
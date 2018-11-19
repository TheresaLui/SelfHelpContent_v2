<properties
	pageTitle="Connectivity issue on blob"
	description="Connectivity issue on blob scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602725,32602734,32602735"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Blob connectivity issue
---
{
    "resourceRequired": true,
    "title": "Connectivity issue on blob scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "blob_or_container",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Container name or Blob path",
            "watermarkText": "'ContainerName' or 'ContainerName/../BlobName' if specific to a container or blob",
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
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> to troubleshoot peformance issues."
        }
    ]
}
---
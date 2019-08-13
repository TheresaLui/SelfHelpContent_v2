<properties
	pageTitle="Blob tiers - Hot, Cool, Archive scoping questions"
	description="Blob tiers - Hot, Cool, Archive scoping questions"
	authors="passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602719,32602732,32602720,32608636,32639221"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="4B46FE3E-420A-4916-B059-A6C939025930"
/>
# Storage block blob tiers
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob tiers - Hot, Cool, Archive scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "blob_type",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Type of blob(s) with tiering issues",
            "watermarkText": "Blob type(s)",
            "dropdownOptions": [
                {
                    "value": "block_blob",
                    "text": "Block Blob(s)"
                },
                {
                    "value": "append_blob",
                    "text": "Append Blob(s)"
                },
                {
                    "value": "page_blob",
                    "text": "Page Blob(s)"
                }
            ],
            "required": false
        },
        {
            "id": "blob_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Blob path",
            "watermarkText": "Sample blob path with tiering issues",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
<properties
	pageTitle="Performance issue on blob"
	description="Performance issue on blob scoping question"
	authors="ramMSFT"
    ms.author="raprasad"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602726,32602727"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="51f6b586-c2a9-4744-b7d3-8f01cef66201"
/>
# Blob performance issue
---
{
    "resourceRequired": true,
    "title": "Performance issue on blob scoping question",
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
            "id": "request_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Storage server Request ID",
            "watermarkText": "Request ID of failed operation ending with 000000",
            "textPropertyRegex":"^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
            "required": false
        },
        {
            "id": "blob_container",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Blob Container",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "NoBlobContainer",
                    "text": "Not specific to a blob container"
                }
            ],
            "required": false
        },
        {
            "id": "blob_path",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Blob path",
            "watermarkText": "Blob name or path if specific to a blob",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 6,
            "controlType": "infoblock",
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> to troubleshoot peformance issues."
        }
    ]
}
---
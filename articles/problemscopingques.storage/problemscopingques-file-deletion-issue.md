<properties
	pageTitle="Storage File share or path"
	description="Storage File share or path scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602743"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File share or path scoping question
---
{
    "resourceRequired": true,
    "title": "Storage File share or path scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "file_share_or_path",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "File Share or File path",
            "watermarkText": "'FileShare' or 'FileShare/FileName'",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": false
        },
        {
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
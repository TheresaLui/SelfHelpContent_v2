<properties
	pageTitle="Storage migration between Storage Accounts"
	description="Storage migration between Storage Accounts scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602736"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="db69e7ff-4d73-423a-97ae-b30cee9f0d64"
/>
# Storage migration between Storage Accounts
---
{
    "resourceRequired": false,
    "title": "Storage migration between Storage Accounts scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_from",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Source Storage Account",
            "watermarkText": "From StorageAccountName",
            "required": false
        },
        {
            "id": "storage_account_to",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Destination Storage Account",
            "watermarkText": "To StorageAccountName",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
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
    ]
}
---

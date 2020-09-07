<properties
	articleId="problemscopingques-sqlmi-backuprestore-databaserestore"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture managed instance database restore information"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637256"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "SQL Database Managed Instance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "error_code",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Error code or error message?",
            "watermarkText": "Provide the error code or error message",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "latest_restore",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Latest time you started the restore?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
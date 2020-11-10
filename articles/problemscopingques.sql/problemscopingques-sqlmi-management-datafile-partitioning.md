<properties
	articleId="problemscopingques-sqlmi-management-datafile-partitioning"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture scaling issues"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637250"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
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
            "id": "operations",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "What action are you trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Database file/filegroup",
                    "text": "Configuring the database file/filegroup layout"
                },
                {
                    "value": "Database partition",
                    "text": "Configuring database partition(s)"
                },
                {
                    "value": "Shrink database",
                    "text": "Shrinking a database"
                },
                {
                    "value": "TempDB",
                    "text": "TempDB-related operations"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message (if any) are you getting?",
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
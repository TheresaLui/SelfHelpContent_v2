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

```json
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
            "displayLabel": "Which issue are you facing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Database file/filegroup",
                    "text": "You encounter an error when configuring the database file/filegroup"
                },
                {
                    "value": "Database partition",
                    "text": "You encounter an error when configuring database partition"
                },
                {
                    "value": "Shrink database",
                    "text": "You encounter an error when shrinking the database"
                },
                {
                    "value": "Tempdb",
                    "text": "You encounter an error on tempdb"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"                
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

```
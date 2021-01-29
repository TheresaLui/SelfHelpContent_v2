<properties
	articleId="problemscopingques-sql-datasync"
	pageTitle="SQL Data Sync"
	description="Scoping questions to capture sync group name"
	authors="vitomaz-msft"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630455"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# SQL Data Sync
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SQL Data Sync",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "SQL Data Sync diagnostics",
        "description": "These diagnostics will check for common errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "syncgroupname",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Sync Group facing the issue",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/syncgroups?api-version=2015-05-01-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Could not find any sync group in this hub",
                    "text": "Could not find any sync group in this hub"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "recently_migrated",
            "order": 21,
            "controlType": "dropdown",
            "displayLabel": "Have you recently migrated to Azure?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "application_type",
            "order": 22,
            "controlType": "dropdown",
            "displayLabel": "What is the application type? ",
            "visibility": "recently_migrated == Yes",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "modern_platform",
                    "text": "Modern distributed platform (Ex: .Net, Java, Python, Ruby etc.)"
                },
                {
                    "value": "legacy",
                    "text": "Legacy (Ex: COBOL, PL-I, Assembler etc.)"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "migration_backend",
            "order": 23,
            "controlType": "dropdown",
            "displayLabel": "What was the Pre-Migration backend ?  ",
            "visibility": "recently_migrated == Yes",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "sql_server",
                    "text": "SQL Server"
                },
                {
                    "value": "oracle",
                    "text": "Oracle"
                },
                {
                    "value": "db2",
                    "text": "DB2"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
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
    ],
    "$schema": "SelfHelpContent"
}
---

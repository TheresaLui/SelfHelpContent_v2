<properties
	articleId="problemscopingques-sqlmi-perf-block-deadlock"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture managed instance issues related to blocking and deadlocks"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739489"
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
            "id": "latest_occurrence",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Latest occurrence of the issue?",
            "required": true
        },
        {
            "id": "frequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Can you reproduce this performance issue consistently?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "consistently",
                    "text": "Yes, consistently"
                },
                {
                    "value": "randomly",
                    "text": "No, randomly"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "database_name",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "What database is having issues?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "{resourceid}/databases?api-version=2017-03-01-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of databases",
                    "text": "Unable to get the list of databases"
                }
            ],
            "required": false
        },
        {
            "id": "db_migrated",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Was this database migrated to Azure recently?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": false
        },
        {
            "id": "index_maintenance",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "maintenance of indexes and statitics is frequent?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": false
        },
        {
            "id": "latest_indexes_defrag",
            "order": 50,
            "visibility" : "index_maintenance == yes",
            "controlType": "datetimepicker",
            "displayLabel": "When was the last indexes and statistics maintenance?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Specific Query Store query_id, plan hash, query hash or query text.",
            "watermarkText": "Provide addicional information about the query or queries facing the issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---

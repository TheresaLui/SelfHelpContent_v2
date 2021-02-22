<properties
	articleId="problemscopingques-sqldb-perf-block-deadlock"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to blocking and deadlocks"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749512"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "SQL Database",
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
            "id": "is_reproducible",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Is the problem reproducible?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes, we can reproduce the problem consistently"
                },
                {
                    "value": "no",
                    "text": " No. The problem occurs randomly"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "transaction_isolation_hint",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Is the transaction isolation level set in the API or in query hints?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "not_set",
                    "text": "Not set"
                },
                {
                    "value": "dontknow",
                    "text": "Dont't know"
                },
                {
                    "value": "set_read_uncommitted",
                    "text": "Yes, set to READ UNCOMMITTED"
                },
                {
                    "value": "set_read_committed",
                    "text": "Yes, set to READ COMMITTED"
                },
                {
                    "value": "set_repeatable",
                    "text": "Yes, set to REPEATABLE"
                },
                {
                    "value": "set_snapshot",
                    "text": "Yes, set to SNAPSHOT"
                },
                {
                    "value": "set_serializable",
                    "text": " Yes, set to SERIALIZABLE"
                }
            ],
            "required": false
        },
        {
            "id": "lock_timeout_hint",
            "order": 60,
            "controlType": "dropdown",
            "displayLabel": "Do you have the LOCK_TIMEOUT set in your connection?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "is_set",
                    "text": "Yes (Please enter timeout value in the textbox below)"
                },
                {
                    "value": "not_set",
                    "text": "No"
                },
                {
                    "value": "dontknow",
                    "text": "Don't know"
                }
            ],
            "required": false
        },
         {
            "id" : "lock_timeout_hint_value",
            "order" : 61,
            "visibility" : "lock_timeout_hint == is_set",
            "controlType" : "textbox",
            "displayLabel" : "Please enter LOCK_TIMEOUT value",
            "watermarkText" : "Enter timeout value (in milliseconds)",
            "required": true
        },
        {
            "id": "indexstat_maintenance",
            "order": 70,
            "controlType": "radioButtonGroup",
            "displayLabel": "How frequent are the indexes and statistics maintained?",
            "watermarkText": "Choose an option",
            "radioButtonOptions": [
                {
                    "value": "daily",
                    "text": "Daily"
                },
                {
                    "value": "weekly",
                    "text": "Weekly"
                },
                {
                    "value": "monthly",
                    "text": "Monthly"
                },
                {
                    "value": "every_few_months",
                    "text": "Every few months"
                },
                {
                    "value": "not_maintained",
                    "text": "Not maintained"
                },
                {
                    "value": "other",
                    "text": "Other (Please describe in the text box below)"
                }
            ],
            "required": false
        },
        {
            "id" : "indexstat_maintenance_other",
            "order" : 71,
            "visibility" : "indexstat_maintenance == other",
            "controlType" : "textbox",
            "displayLabel" : "Please describe index/statistics maintenance frequency",
            "watermarkText" : "Describe other",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.  If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---

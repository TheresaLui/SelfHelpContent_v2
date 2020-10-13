<properties
	articleId="problemscopingques-sqldb-perf-managing-for-db-and-pools"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to managing space and pools"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749518"
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
            "order": 10,
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
                    "text": "No.  The problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "observed_problem",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Which problem or topic are you observing.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "is_on",
                    "text": "Shrinking file(s)"
                },
                {
                    "value": "is_off",
                    "text": "Allocating file space"
                },
                {
                    "value": "dont_know",
                    "text": "Other (Please describe in Description)"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for your space management for database and pools.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Additional context."
        }
    ]
}
---

<properties
	articleId="problemscopingques-sqlmi-perf-managing-for-db-and-pools"
	pageTitle="Azure SQL Database Managed Instance"
	description="Scoping questions to capture issues related to managing space and pools"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748870"
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
                    "text": "No. The problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "observed_problem",
            "order": 30,
            "controlType": "radioButtonGroup",
            "displayLabel": "Which problem or topic are you observing?",
            "watermarkText": "Choose an option",
            "radioButtonOptions": [
                {
                    "value": "reducing_db_size",
                    "text": "Reducing database size, shrinking file(s)"
                },
                {
                    "value": "allocate_file_space",
                    "text": "Allocating file space"
                },
                {
                    "value": "other",
                    "text": "Other (Describe in the following text box)"
                }
            ],
            "required": false
        },
        {
            "id" : "observed_problem_other",
            "order" : 31,
            "visibility" : "observed_problem == other",
            "controlType" : "textbox",
            "displayLabel" : "Describe the problem you're seeing",
            "watermarkText" : "Problem observed",
            "required": true
        },
        {
            "id": "is_tempdb_issue",
            "order": 40,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is this a tempdb database issue?",
            "watermarkText": "Choose an option",
            "radioButtonOptions": [
                {
                    "value": "is_tempdb_issue",
                    "text": "Yes"
                },
                {
                    "value": "is_otherdb_issue",
                    "text": "No, other than tempdb"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional context for your space management of database and pools.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Additional context."
        }
    ]
}
---

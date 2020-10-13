<properties
	articleId="problemscopingques-sqldb-perf-high-io-utilization"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to high IO utilization"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749515"
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
                    "text": "No. The problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "event_prior_to_high_io",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "To the best of your knowledge, which event took place prior to observing the high IO.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "event_migration",
                    "text": "Migrated database from On Premises database"
                },
                {
                    "value": "event_reconfigure_slo",
                    "text": "Reconfigured the database Service Level Objective (SLO)"
                },
                {
                    "value": "event_change_db_option",
                    "text": "Changed the database option"
                },
                {
                    "value": "event_index_maintenance",
                    "text": "Index maintenance"
                },
                {
                    "value": "event_other",
                    "text": "Others (Please describe in Description)"
                }
            ],
            "required": false
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

<properties
	articleId="problemscopingques-sqldb-perf-high-cpu-utilization"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to high CPU utilization"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749514"
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
                    "text": " No.  The problem occurs randomly"
                }               
            ],
            "required": false
        },
        {
            "id": "cpu_spike",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Is the high CPU a sudden spike or observing 70% or higher over certain periods?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "sudden_spike",
                    "text": "Sudden spike"
                },
                {
                    "value": "periodic_spike",
                    "text": "Observing 70% or higher over certain periods"
                },
                {
                    "value": "other_spike",
                    "text": "Other (Please describe in Description)"
                }
            ],
            "required": false
        },
        {
            "id": "event_prior_to_spike",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "To the best of your knowledge, which event took place prior to observing the high CPU utilization. ",
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
                    "value": "event_change_app_code",
                    "text": "Change in the application code"
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

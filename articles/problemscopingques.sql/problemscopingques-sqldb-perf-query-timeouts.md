<properties
	articleId="problemscopingques-sqldb-perf-query-timeouts"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to Query Timeouts"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749520"
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
                    "text": "No.  The problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "observed_recent_event",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "If applicable, please select recent events prior to observing the query timeouts.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "event_migration",
                    "text": "Migrated database from On-Premises database"
                },
                {
                    "value": "event_slo",
                    "text": "Reconfiguration of the database Service Level Objective (SLO)"
                },
                {
                    "value": "event_change_db_option",
                    "text": "Changed database option"
                },
                {
                    "value": "event_change_app_code",
                    "text": "Changed application code"
                },
                {
                    "value": "event_index_maintenance",
                    "text": "Index maintenance (Index rebuild/reorganize)"
                },
                {
                    "value": "event_other",
                    "text": "Others (Please describe in the following text box)"
                },
                {
                    "value": "event_unkown",
                    "text": "Not aware"
                }
            ],
            "required": false
        },
         {
            "id" : "observed_recent_event_other",
            "order" : 31,
            "visibility" : "observed_recent_event == event_other",
            "controlType" : "textbox",
            "displayLabel" : "Please describe event observed",
            "watermarkText" : "Events observed",
            "required": true
        },
        {
            "id": "application_type",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Is your application developed using any type of object-relational mapper such as Entity Framework?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "app_entity_framework",
                    "text": "Yes, using Entity Framework"
                },
                {
                    "value": "app_custom",
                    "text": "No, we are using customized application"
                },
                {
                    "value": "app_third_party",
                    "text": "No, we are using third party application"
                },
                {
                    "value": "app_not_applicable",
                    "text": "Not applicable"
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

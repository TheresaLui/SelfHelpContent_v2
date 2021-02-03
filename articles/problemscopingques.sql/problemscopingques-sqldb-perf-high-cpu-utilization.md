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
                    "text": "Other (Please describe in the following text box)"
                }
            ],
            "required": false
        },
        {
            "id" : "cpu_spike_other",
            "order" : 31,
            "visibility" : "cpu_spike == other_spike",
            "controlType" : "textbox",
            "displayLabel" : "Please describe symptoms of the CPU utilization observed.",
            "watermarkText" : "Symptoms observed",
            "required": true
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
                    "text": "Migrated database from On-Premises database"
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
                    "text": "Others (Please describe in the following text box)"
                }
            ],
            "required": false
        },
        {
            "id" : "event_prior_to_spike_other",
            "order" : 41,
            "visibility" : "event_prior_to_spike == event_other",
            "controlType" : "textbox",
            "displayLabel" : "Please describe events observed",
            "watermarkText" : "Events observed",
            "required": true
        },
        {
            "id" : "application_type",
            "order" : 42,
            "visibility" : "event_prior_to_spike == event_migration",
            "controlType" : "dropdown",
            "displayLabel" : "What is the application type?",
            "watermarkText": "Choose an option",
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
            "id" : "migration_backend",
            "order" : 43,
            "visibility" : "event_prior_to_spike == event_migration",
            "controlType" : "dropdown",
            "displayLabel" : "What was the Pre-Migration backend?",
            "watermarkText": "Choose an option",
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
            "displayLabel": "Please provide additional context for the high CPU utilization observed.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---

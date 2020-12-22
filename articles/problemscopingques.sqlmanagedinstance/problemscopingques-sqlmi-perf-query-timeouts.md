<properties
	articleId="problemscopingques-sqlmi-perf-query-timeouts"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture issues related to Query Timeouts"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748872"
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
    "title": "Query Timeout",
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
                    "text": "Reconfiguration of the instance Service Level Objective (SLO)"
                },
                {
                    "value": "event_change_server_option",
                    "text": "Changed server option"
                },
                {
                    "value": "event_change_app_code",
                    "text": "Changed application code"
                },
                {
                    "value": "event_index_maintenance",
                    "text": "Index maintenance (Index rebuild/reorganize/drop, stats update)"
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
            "id": "application_Entity_type",
            "order": 40,
            "visibility" : "observed_recent_event != event_migration",
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
            "id" : "application_migration_type",
            "order" : 41,
            "visibility" : "observed_recent_event == event_migration",
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
            "order" : 42,
            "visibility" : "observed_recent_event == event_migration",
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
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.  If available, attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---

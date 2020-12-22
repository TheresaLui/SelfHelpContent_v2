<properties
	articleId="problemscopingques-sqlmi-perf-query-tuning"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture issues related to Query Tuning"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748873"
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
    "title": "Query tuning",
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
            "id": "is_query_for_tuning_identified",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Is the query that requires tuning specifically identified?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes_all_identified",
                    "text": "Yes, all queries are identified"
                },
                {
                    "value": "yes_some_identified",
                    "text": "Yes, but there could be other queries that require tuning."
                },
                {
                    "value": "dont_know_answer",
                    "text": "No, not sure"
                }
            ],
            "required": true
        },
        {
            "id": "query_characteristics",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Which type resembles the characteristics of the queries?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "qry_oltp",
                    "text": "OLTP (Primarily INSERT/UPDATE/DELETE operation)"
                },
                {
                    "value": "qry_olap",
                    "text": "OLAP (Primarily READ operation)"
                },
                {
                    "value": "qry_oltp_olap",
                    "text": "Mixture of both OLTP and OLAP types"
                },
                {
                    "value": "qry_unknown",
                    "text": "Not sure"
                },
                {
                    "value": "qry_other",
                    "text": "Others (Please describe in the following text box)"
                }
            ],
            "required": false
        },
        {
            "id" : "query_characteristics_other",
            "order" : 30,
            "visibility" : "query_characteristics == qry_other",
            "controlType" : "textbox",
            "displayLabel" : "Please describe the query characteristics.",
            "watermarkText" : "Query characteristics",
            "required": true
        },
        {
            "id": "baseline_exists",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Is there a baseline established for the query performance?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "have_baseline",
                    "text": "Yes, we have a baseline for the query performance"
                },
                {
                    "value": "no_baseline",
                    "text": "No, or not sure if we have any"
                }
            ],
            "required": false
        },
        {
            "id": "application_type",
            "order": 50,
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
            "id": "observed_recent_event",
            "order": 60,
            "controlType": "dropdown",
            "displayLabel": "If applicable, please select recent events prior to observing the query performance reduction.",
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
            "order" : 70,
            "visibility" : "observed_recent_event == event_other",
            "controlType" : "textbox",
            "displayLabel" : "Please describe event observed",
            "watermarkText" : "Events observed",
            "required": true
        },
        {
            "id" : "application_migration_type",
            "order" : 80,
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
            "order" : 90,
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
            "displayLabel": "Please describe the criteria for the successful query tuning.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Description the criteria for the query tuning"
        }
    ]
}
---

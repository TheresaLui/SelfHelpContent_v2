<properties
	articleId="problemscopingques-sqldb-perf-query-tunning"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to Query Tunning"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749521"
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
            "displayLabel": "Is the query that requires tunning specifically identified?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes_all_identified",
                    "text": "Yes, all queries are identified"
                },
                {
                    "value": "yes_some_identified",
                    "text": "Yes, but there could be other queries that require tunning."
                },
                {
                    "value": "no",
                    "text": "No, not sure"
                }
            ],
            "required": false
        },
        {
            "id": "observed_recent_event",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Which type resembles the characteristics of the queries.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "event_migration",
                    "text": "OLTP (Primarily INSERT/UPDATE/DELETE operation)"
                },
                {
                    "value": "event_slo",
                    "text": "ROLAP (Primarily READ operation)"
                },
                {
                    "value": "event_change_db_option",
                    "text": " Both, OLTP and OLAP"
                },
                {
                    "value": "event_change_app_code",
                    "text": "Not sure, or not applicable (Please describe in the Description)"
                }
            ],
            "required": false
        },
          {
            "id": "baseline_exists",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Is there a baseline established for the query performance?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "event_migration",
                    "text": "Yes, we have a baseline for the query performance"
                },
                {
                    "value": "event_slo",
                    "text": "No, or not sure if we have any"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the criteria for the successful query tunning.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Description of your criteria for the query tunning"
        }
    ]
}
---

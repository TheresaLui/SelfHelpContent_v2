<properties
	articleId="problemscopingques-sqldb-perf-query-tunning"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to Query Tuning"
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
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "is_query_for_tuning_identified",
            "order": 20,
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
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Which type resembles the characteristics of the queries.",
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
            "order" : 31,
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
            "id": "application_type",
            "order": 45,
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
            "displayLabel": "Please describe the criteria for the successful query tuning.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Description the criteria for the query tuning"
        }
    ]
}
---

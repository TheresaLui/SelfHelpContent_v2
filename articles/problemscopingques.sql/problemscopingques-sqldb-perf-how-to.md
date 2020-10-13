<properties
	articleId="problemscopingques-sqldb-perf-how-to"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to How To"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749516"
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
            "id": "what_topic",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Which topic are you interested in knowing.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "howto_dmv",
                    "text": "How to use DMVs to monitor performance"
                },
                {
                    "value": "hotwo_query_store",
                    "text": "How to use Query Store to monitor performance"
                },
                {
                    "value": "howto_apply_performance_recommendations",
                    "text": "How to apply performance recommendations and optimize your database"
                },
                {
                    "value": "howto_troubleshoot_perf_insight",
                    "text": "Troubleshoot performance with Intelligent Insights"
                },
                {
                    "value": "howto_other",
                    "text": "Other (Please describe in Description)"
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

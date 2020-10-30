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
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
         {
            "id": "what_topic",
            "order": 20,
            "controlType": "radioButtonGroup",
            "displayLabel": "Which topic are you interested in knowing.",
            "watermarkText": "Choose an option",
            "radioButtonOptions": [
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
                    "text": "Other (Please describe in the following text box)"
                }
            ],
            "required": false
        },
        {
            "id" : "what_topic_other",
            "order" : 21,
            "visibility" : "what_topic == howto_other",
            "controlType" : "textbox",
            "displayLabel" : "Please provide topic of interest or facing problem.",
            "watermarkText" : "Enter topic or facing problem",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the topic of interest or the facing problem ",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "If available, please attach any relevant screenshots or URL referenced"
        }
    ]
}
---

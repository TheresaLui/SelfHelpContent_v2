<properties
	articleId="problemscopingques-sqlmi-perf-block-deadlock"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture managed instance issues related to blocking and deadlocks"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739489"
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
    "title": "SQL Database Managed Instance",
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
            "id": "latest_occurrence",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Latest occurrence of the issue?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Specific Query Store query_id, plan hash, query hash or query text.",
            "watermarkText": "Provide addicional information about the query or queries facing the issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---

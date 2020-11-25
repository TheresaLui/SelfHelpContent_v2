<properties
    pageTitle="Database Performance"
    description="Database Performance"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640026, 32781013, 32781014"
    productPesIds="17067,17068,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-perf-unexpectedbehavior"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Performance and Query Execution - Unexpected behavior, errors or exceptions executing a query
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Performance Unexpected behavior",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Perf Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Perf Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Following the steps in Recommended Solution section below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please provide the repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "client_driver",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the name and version of the client driver you are using?",
            "required": false
        },
        {
            "id": "error_message",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the error message you received?",
            "required": false
        },
        {
            "id": "result_size",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the result size of the query normally?",
            "required": false
        },
        {
            "id": "sample_queries",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Can you please share one of the sample queries?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---

<properties
    pageTitle="Migrating to Azure"
    description="Migrating to Azure"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639991, 32639996, 32780999, 32781000, 32781002, 32781003, 32731226"
    productPesIds="16222,17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-migrating-issuestools"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Migrating to Azure - Issues with migration & Migration tools
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Migrating to Azure Issues",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Migrating to Azure Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Migrating to Azure Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "env_migrate_from",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the environment you are migrating your server from?",
            "required": false
        },
        {
            "id": "server_type",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the server type/server version of your source server?",
            "required": false
        },
        {
            "id": "server_size",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the size of your source database server?",
            "required": false
        },
        {
            "id": "tool_migrate",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the tool you are using for migration?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please provide the repro steps and other information about your issue",
            "required": true,
            "diagnosticInputRequiredClients": "Portal",
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---

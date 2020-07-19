<properties
    pageTitle="Migrating to Azure"
    description="Migrating to Azure"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639991,32639996"
    productPesIds="17067,17069,17068"
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
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "env_migrate_from",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the environment you are migrating your server from?",
            "required": false
        },
        {
            "id": "server_type",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the server type/server version of your source server?",
            "required": false
        },
        {
            "id": "server_size",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the size of your source database server?",
            "required": false
        },
        {
            "id": "tool_migrate",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the tool you are using for migration?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---

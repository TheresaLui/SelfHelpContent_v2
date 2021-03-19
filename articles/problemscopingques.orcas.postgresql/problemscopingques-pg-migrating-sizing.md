<properties
    pageTitle="Migrating to Azure"
    description="Migrating to Azure"
    authors="Joe Nelson"
    ms.author="jonels"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32731224"
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-migrating-sizing"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Migrating to Azure - Choosing a server group size
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Migrating to Azure - Choosing server group size",
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
            "displayLabel": "When did you begin planning your migration?",
            "infoBalloonText": "Enter the approximate date.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "server_size",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the size of the data in your source database server?",
            "required": false
        },
        {
            "id": "server_ram",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How much RAM does your source database server have?",
            "required": false
        },
        {
            "id": "server_cores",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "How many CPU cores does your source database server have?",
            "required": false
        },
        {
            "id": "server_latency",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the average latency for typical queries on your source database server?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Workload",
            "watermarkText": "Please describe your database workload and scaling needs",
            "required": true,
            "diagnosticInputRequiredClients": "Portal",
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---

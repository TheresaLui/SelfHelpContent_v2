<properties
    pageTitle="Migrating to Azure"
    description="Migrating to Azure"
    authors="Joe Nelson"
    ms.author="jonels"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32731225"
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-migrating-modeling"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Migrating to Azure - Help with data modeling
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Migrating to Azure - help with modeling",
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
            "displayLabel": "When did you start thinking about data modeling for your migration?",
            "infoBalloonText": "Enter the approximate date.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "schema_table_count",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Roughly how many tables are in your existing schema?",
            "required": false
        },
        {
            "id": "schema_tenancy",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Does your database serve multiple tenants? If so, what are they (companies, accounts, etc)?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please describe your data modeling goals and challenges.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal",
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---

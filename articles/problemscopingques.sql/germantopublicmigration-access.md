<properties
	articleId="427a0459-7468-49d0-9da5-111aa863ecfe"
	pageTitle="SQL Database"
	description="Scoping questions for Migration from Microsoft Cloud Germany to global Azure"
	authors="subbuk"
	authoralias="subbuk"
	ms.author="subbuk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32785509"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
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
            "id": "sqlexception_received_on_client",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide subscription(s) pairs for allow listing. (Obscure the personally identifiable information).",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Migration Details",
            "watermarkText": "Provide source (Germany Cloud) and target (Azure global) subscription IDs to enable Geo-Replication method to migrate your database." ,
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---

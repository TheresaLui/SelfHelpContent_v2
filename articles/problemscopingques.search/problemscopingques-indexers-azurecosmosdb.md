<properties
	pageTitle="Issue indexing data from an Azure Cosmos DB data source"
	description="Issue indexing data from an Azure Cosmos DB data source"
	authors="maheff"
	ms.author="maheff"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681364"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="9d1eb2ee-ad58-47ae-b75f-3f50bf8889e4"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue indexing data from an Azure Cosmos DB data source
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue indexing data from an Azure Cosmos DB data source",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the issue.",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did this issue occur?",
            "required": true
        },
        {
            "id": "indexer_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the name of the indexer that had this issue?",
            "required": true
        },
        {
            "id": "indexing_error_message",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
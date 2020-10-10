<properties
	pageTitle="Issue indexing data from an Azure Blob Storage data source"
	description="Issue indexing data from an Azure Blob Storage data source"
	authors="maheff"
	ms.author="maheff"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681363"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="0878deda-9364-419a-a126-bf6d20fad336"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue indexing data from an Azure Blob Storage data source
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue indexing data from an Azure Blob Storage data source",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did this issue occur?",
            "required": true
        },
        {
            "id": "indexing_error_message",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "indexing_error_message",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of the indexer that had this issue?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "useAsAdditionalDetails": false,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
<properties
	pageTitle="Issue indexing data from an Azure Table Storage data source"
	description="Issue indexing data from an Azure Table Storage data source"
	authors="maheff"
	ms.author="maheff"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681366"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="0a33832f-f854-4b25-afaf-164729a3a9c7"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue indexing data from an Azure Table Storage data source
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue indexing data from an Azure Table Storage data source",
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
<properties
	pageTitle="CosmosDB PITR scoping questions"
	description="CosmosDB PITR scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32787635"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="229f46c7-b4c9-4d2a-8ae3-6024f1d9e441"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Database and Collection Info
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cosmos DB Point in Time Restore",
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
            "id": "database_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
        {
            "id": "collection_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional details about the issue that you are encountering",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---

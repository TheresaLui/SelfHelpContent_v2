<properties
	pageTitle="CosmosDB Monitoring scoping questions"
	description="CosmosDB Monitoring scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636767,32681014,32783704,32636799,32741538,32788300"
    productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="cc1f6862-e3a3-4cac-9cc5-bf005a3eaa24"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Monitoring
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Monitoring",
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
            "id": "tabs_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Tab name",
            "required": false
        },
        {
            "id": "metric_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Metric name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Read/Write regions where the issue is experienced"
                },
                {
                    "text": "Activity Id of the request (if available)."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---

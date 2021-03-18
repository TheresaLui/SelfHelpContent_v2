<properties
	pageTitle="CosmosDB Default scoping questions"
	description="CosmosDB Default scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636764,32636765,32636772,32636773,32636781,32636791,32636793,32636794,32636797,32636798,32636800,32741532,32741533,32636820,32636824,32636826,32636828,32636829,32675639,32675640,32675641,32675642,32681006,32681007,32684531,32684532,32688845,32741327,32741539,32692540,32692544,32738666,32741326,32741540,32746032,32746033,32747698,32783699,32783700,32783727"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="076846c1-4c0b-4b21-91c6-1a30246b3867"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Database and Collection Info
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Database and Collection Info",
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

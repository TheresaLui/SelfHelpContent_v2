<properties
	pageTitle="CosmosDB Synapse Link scoping questions"
	description="CosmosDB Synapse Link scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32742612,32742613,32742614,32742615,32743028,32743029,32743053,32743054,32743055,32743056,32743057,32743058,32743059,32783706"
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="406206a0-1298-44a3-a971-40339d142392"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Azure Synapse Link for Cosmos DB
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
            "id": "synapselink_workspace_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Synapse Link workspace name",
			"infoBalloonText": "Azure Synapse Link workspace name",
            "required": false
        },
		{
            "id": "synapselink_region",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Synapse Link Region",
			"infoBalloonText": "Azure Synapse Link Region",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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

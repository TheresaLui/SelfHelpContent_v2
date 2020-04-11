<properties
	pageTitle="Cosmos DB Private Link scoping questions"
	description="Cosmos DB Private Link scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32738665,32738664"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="473999a4-feeb-42ce-95e1-b1559b34d2b2"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Private Link
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
            "id": "resource_Id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Resource Id of the private endpoint",
            "required": false
        },
		{
            "id": "priavate_ZoneUsage",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you using Azure Private Zones in the virtual network?",
			"watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
		{
            "id": "PrivateZone_Id",
            "order": 6,
			"visibility": "priavate_ZoneUsage == Yes",
			"controlType": "textbox",
			"displayLabel": "Private Zone Id",
			"required": false
        },
		{
            "id": "connection_mode",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to connect in gateway or direct mode?",
			"watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Gateway",
                    "text": "Gateway"
                },
                {
                    "value": "Direct",
                    "text": "Direct"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": false
        },
		{
            "id": "added_region",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Did you recently add a new region?",
			"watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
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

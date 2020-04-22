<properties
	pageTitle="CosmosDB Core SQL High Latency scoping questions"
	description="CosmosDB Core SQL High Latency scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32688844"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="71fccbe7-16b1-4933-bd89-33b0eaf2721a"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Core SQL High Latency Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Database and Collection Info",
    "fileAttachmentHint": "Please attach exception or diagnostic string if available.",
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
            "id": "connection_mode",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Client connection mode",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Direct",
                    "text": "Direct"
                },
                {
                    "value": "Gateway",
                    "text": "Gateway"
                }
            ],
            "required": false
        },
		{
            "id": "protocol_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Client Protocol",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Http",
                    "text": "Http"
                },
                {
                    "value": "TCP",
                    "text": "TCP"
                }
            ],
            "required": false
        },
		{
            "id": "preferredlocation_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Preferred Location",
			"infoBalloonText": "<a href='https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.preferredlocations'>Cosmos DB article</a> -PreferredLocations Property",
            "required": false
        },
		{
            "id": "clientlocation_name",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Client Location",
			"infoBalloonText": "The country region the client application is running",
            "required": false
        },
		{
            "id": "requestkind_name",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Request kind",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create",
                    "text": "Create"
                },
                {
                    "value": "Read",
                    "text": "Read"
                },
                {
                    "value": "Replace",
                    "text": "Replace"
                },
                {
                    "value": "Upsert",
                    "text": "Upsert"
                },
                {
                    "value": "Delete",
                    "text": "Delete"
                },
                {
                    "value": "Query",
                    "text": "Query"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing",
			"infoBalloonText": "<a href='https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.resourceresponsebase.requestdiagnosticsstring'>Cosmos DB article</a> -RequestDiagnosticsString Property",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Request diagnostic string"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
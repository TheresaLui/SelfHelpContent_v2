<properties
	pageTitle="CosmosDB SQL Query Issue"
	description="CosmosDB SQL Query Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636818,32636795,32636821,32681012, 32681470"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="cdd74fa9-ba72-4dab-8b4e-82d7f6a4e5bc"
/>
# CosmosDB SQL Query Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB SQL Query Issue",
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
            "id": "query_text",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "SQL Query Text",
            "required": true,
            "useAsAdditionalDetails": false
        },
		{
            "id": "query_metrics",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Query Metrics or Activity Id",
			"infoBalloonText": "<a href='https://docs.microsoft.com/azure/cosmos-db/profile-sql-api-query'>Cosmos DB article</a> -How to Get SQL query execution metrics and analyze query performance using .NET SDK",
            "required": false
        },
		{
            "id": "indexing_policy",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Collection Indexing Policy",
			"infoBalloonText": "<a href='https://docs.microsoft.com/azure/cosmos-db/index-policy'>Cosmos DB article</a> -Indexing policies in Azure Cosmos DB",
            "required": false,
            "useAsAdditionalDetails": false
        },
		{
            "id": "sdk_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the client SDK used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": ".NET",
                    "text": ".NET"
                },
                {
                    "value": "Java",
                    "text": "Java"
                },
                {
                    "value": "Node.js",
                    "text": "Node.js"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "REST",
                    "text": "REST"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1xx, 2xx, 3xx)",
            "required": false
        },
		{
            "id": "MaxItemCount",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "MaxItemCount",
			"infoBalloonText": "<a href='https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.feedoptions.maxitemcount?view=azure-dotnet#Microsoft_Azure_Documents_Client_FeedOptions_MaxItemCount'>Cosmos DB article</a> -MaxItemCount",
            "required": false
        },
		{
            "id": "MaxBufferedItemCount",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "MaxBufferedItemCount",
			"infoBalloonText": "<a href='https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.feedoptions.maxbuffereditemcount?view=azure-dotnet#Microsoft_Azure_Documents_Client_FeedOptions_MaxBufferedItemCount'>Cosmos DB article</a> -MaxBufferedItemCount",
            "required": false
        },
		{
            "id": "MaxDegreeOfParallelism",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "MaxDegreeOfParallelism",
			"infoBalloonText": "<a href='https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.feedoptions.maxdegreeofparallelism?view=azure-dotnet#Microsoft_Azure_Documents_Client_FeedOptions_MaxDegreeOfParallelism'>Cosmos DB article</a> -MaxDegreeOfParallelism",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Read/Write regions where the issue is experienced"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
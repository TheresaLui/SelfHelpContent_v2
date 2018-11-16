<properties
	pageTitle="CosmosDb Query Performance Issue"
	description="CosmosDb Query Performance Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32597551,32597550,32597549,32597548"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# CosmosDb Query performance Issue
---
{
	"resourceRequired": true,
	"title": "CosmosDb Query Performance Issue",
	"fileAttachmentHint": "",
	"formElements": [
			{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "Use the <a href='https://docs.microsoft.com/azure/cosmos-db/performance-tips'>Performance Tuning Guide</a> to learn more about how you can improve the performance of your database"
		},
      		   {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		  },
		  {
			"id": "database_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Database name",
			"required": true,
			"hints": [{
					"text": "Database name"
				}]
		},
		{
			"id": "collection_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Collection name",
			"required": true,
			"hints": [{
					"text": "Collection name"
				}]
		},
		{
			"id": "partition_key",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Collection Partition Key",
			"required": false
		},
		{
			"id": "indexing_policy",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Collection Indexing Policy",
			"required": false,
			"useAsAdditionalDetails": false
		},
		{
			"id": "query_snippet",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Cosmos DB Query snippet",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [
				{
					"text": "Paste the query snippet which is experiencing issues."
				}
			]
		},{
			"id": "sdk_type",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "What is the client SDK used?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": ".NET",
					"text": ".NET"
				},{
					"value": "Java",
					"text": "Java"
				},{
					"value": "Node.js",
					"text": "Node.js"
				},{
					"value": "Python",
					"text": "Python"
				},{
					"value": "Other (describe below)",
					"text": "Other (mention below in the description)"
				}
			],
			"required": false
		},
		  {
			"id": "problem_description",
			"order": 9,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details about the issue that you were facing.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "More information on the exact issue."
				},{
					"text": "Read/Write regions where the issue is experienced"
				},{
					"text": "Activity Id of the request (if available)."
				}
			]
		}
	]
}
---

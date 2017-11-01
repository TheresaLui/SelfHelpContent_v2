<properties
	pageTitle="CosmosDb Performance Issue"
	description="CosmosDb Performance Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32574412"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# CosmosDb performance Issue
---
{
	"resourceRequired": true,
	"title": "CosmosDb Performance Issue",
	"fileAttachmentHint": "",
	"formElements": [
			{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "Use the <a href='https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips'>Performance Tuning Guide</a> to learn more about how you can improve the performance of your database"
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
			"id": "database_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Collection name",
			"required": true,
			"hints": [{
					"text": "Collection name"
				}]
		},
		{
			"id": "sdk_type",
			"order": 5,
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
			"id": "partition_key",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Collection Partition Key",
			"required": false,
			"hints": [{
					"text": "Partition Key of the affected collection"
				}]
		},
    {
			"id": "indexing_policy",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Collection indexing policy.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "Indexing policy for the affected collection."
				}
			]
		},
     {
			"id": "query_snippet",
			"order": 8,
			"controlType": "multilinetextbox",
			"displayLabel": "Query snippet.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "Paste the query snippet."
				}
			]
		},
		  {
			"id": "performance_issue_details",
			"order": 9,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details about the issue that you were facing.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "More information on the exact issue."
				},{
					"text": "Activity Id of the request (if available)."
				},{
					"text": "Read/Write regions where the issue is being experienced."
				}
			]
		}
	]
}
---

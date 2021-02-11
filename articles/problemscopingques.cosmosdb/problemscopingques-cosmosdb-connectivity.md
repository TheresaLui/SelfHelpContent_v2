<properties
	pageTitle="CosmosDB OSS API Service Connectivity Issue"
	description="CosmosDB OSS API Service Connectivity Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636776,32681008,32681470,32636778"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="cf3c77da-f5fa-4052-a0fc-248c65e28885"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB OSS API Service Connectivity  Issue
---
{
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "CosmosDB OSS API Service Connectivity Issue",
	"fileAttachmentHint": "Please attach at least 20 stack traces wtih the exception message in a single flat text file.",
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
			"id": "problem_duration",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "How long was the issue observed?",
			"required": false
		},
		{
			"id": "region_name",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Which region is your client running?",
			"required": false
		},
		{
			"id": "oss_api",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Which API are you using?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
					"value": "Azure Table",
					"text": "Azure Table"
				},
				{
					"value": "Cassandra API",
					"text": "Cassandra API"
				},
				{
					"value": "Core (SQL)",
					"text": "Core (SQL)"
				},
				{
					"value": "Gremlin (Graph)",
					"text": "Gremlin (Graph)"
				},
				{
					"value": "MongoDB",
					"text": "MongoDB"
				},
				{
					"value": "dont_know_answer",
					"text": "I don't know"
				}
			],
			"required": true
		},
		{
			"id": "sdk_type",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Which SDK are you using?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
					"value": ".NET",
					"text": ".NET"
				},
				{
					"value": ".NET Core",
					"text": ".NET Core"
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
					"value": "Spring Boot",
					"text": "Spring Boot"
				},
				{
					"value": "REST",
					"text": "REST"
				},
				{
					"value": "dont_know_answer",
					"text": "I don't know"
				}
			],
			"required": false
		},
		{
			"id": "exception_count",
			"order": 8,
			"controlType": "textbox",
			"displayLabel": "How many service unavailable exceptions did you observe?",
			"required": false
		},
		{
			"id": "vm_count",
			"order": 9,
			"controlType": "textbox",
			"displayLabel": "Number of VMs the exception was seen during this time.",
			"required": false
		},
		{
			"id": "problem_description",
			"order": 10,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide any additional details about the issue that you were facing",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "More information on the exact issue."
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

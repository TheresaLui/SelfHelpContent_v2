<properties
	pageTitle="Azure mapping Data Flow issue info"
	description="Scoping questions to gather mapping data flow issues information"
	ms.author="hecepeda"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32633533,32633532,32633535,32637157,32633536,32633537,32633539,32633540"
	productPesIds="15613"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="mapping-dataflow"
	ownershipId="AzureData_DataFactory"
/>
# Azure mapping Data Flow issue info
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Azure mapping Data Flow issue info",
	"fileAttachmentHint": "Consider attaching screen shots or pipeline json files to help us triage your problem faster",
	"formElements": [
		{
			"id": "problem_description",
			"order": 1,
			"controlType": "multilinetextbox",
			"displayLabel": "Please briefly describe the issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "Is it a new issue or regression?"
				},
				{
				    "text": "Is the issue intermittent or persistent?"
				}
			]
		},
		{
			"id": "error_message",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "What error message do you see?",
			"required": false
		},
		{
			"id": "problem_run_id",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Is this a run time issue? If yes, please provide the Activity RunIDs. (separate with commas)",
			"required": false
		},
		{
			"id": "problem_session_id",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "If this an issue while debugging please provide the SessionID.",
			"required": false
		},
		{
			"id": "problem_start_time",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "What time did the problem begin?",
			"required": true
		}
	]
}
---

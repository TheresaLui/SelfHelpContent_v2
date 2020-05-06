<properties
	pageTitle="Performance and query execution/specific errors or exceptions"
	description="Scoping questions for performance and query execution/specific errors or exceptions"
	ms.author="pedin,xinyl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630454"
	productPesIds="13491"
	articleId="54414786-435A-4A75-8C1F-2BF0BD8E2169"
	cloudEnvironments="public,blackForest,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# Performance and query execution/specific errors or exceptions
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Specific errors or exceptions",
	"fileAttachmentHint": "",
	"diagnosticCard": {
	"title": "SQL DB Performance Troubleshooter",
	"description": "Our SQL DB Performance Troubleshooter can help you troubleshoot and solve your problem.",
	"insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
	},
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
			"required": false,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "error_dropdown",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What error are you seeing?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
					"value": "Error_701",
					"text": "Error 701: There is insufficient system memory to run this query"
				}, {
					"value": "Error_845",
					"text": "Error 845: Time-out occurred while waiting for buffer latch type X for page Y, database ID Z"
				}, {
					"value": "Error_1205",
					"text": "Error 1205: Transaction (Process ID X) was deadlocked on Y"
				}, {
					"value": "Error_9002",
					"text": "Error 9002: The transaction log for database X is full"
				}, {
					"value": "Error_10928",
					"text": "Error 10928: The session limit for the database is X and has been reached"
				}, {
					"value": "Error_10930",
					"text": "Error 10930: The service is currently too busy"
				}, {
					"value": "Error_Other",
					"text": "Other error not listed"
				}, {
					"value": "dont_know_answer",
					"text": "Don't know answer"
				}
			],
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Details of the issue.",
			"watermarkText": "Please provide additional context for the error message you are encountering.",
			"required": true
		}
	]
}
---
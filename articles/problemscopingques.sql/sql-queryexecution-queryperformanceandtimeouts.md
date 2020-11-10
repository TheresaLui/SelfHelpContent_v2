<properties
	pageTitle="Performance and query execution/query performance and timeouts"
	description="Scoping questions for performance and query execution/query performance and timeouts"
	ms.author="pedin,andikshi,xinyl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630450"
	productPesIds="13491"
	articleId="C00BD8E2-3CA0-451D-A2E5-8BE0987A0150"
	cloudEnvironments="public,blackForest,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# Performance and query execution/query performance and timeouts
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Query performance and timeouts",
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
			"displayLabel": "What is the start time of the issue?",
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "What is the end time of the issue? (If ongoing, leave this field blank)",
			"required": false,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "recently_migrated",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Have you recently migrated to Azure?",
			"required": true,
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
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
		}, {
			"id": "application_type",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "What is the application type? ",
			"visibility": "recently_migrated == Yes",
			"required": true,
			"dropdownOptions": [
				{
					"value": "modren_platform",
					"text": "Modern distributed platform (Ex: .Net, Java, Python, Ruby etc.)"
				},
				{
					"value": "legacy",
					"text": "Legacy (Ex: COBOL, PL-I, Assembler etc.)"
				},
				{
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
		}, {
			"id": "migration_backend",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What was the Pre-Migration backend ?  ",
			"visibility": "recently_migrated == Yes",
			"required": true,
			"dropdownOptions": [
				{
					"value": "sql_server",
					"text": "SQL Server"
				},
				{
					"value": "oracle",
					"text": "Oracle"
				},
				{
					"value": "db2",
					"text": "DB2"
				},
				{
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
		}, {
			"id": "problem_description",
			"order": 6,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Specific Query Store query_id, plan hash, query hash or query text.",
			"watermarkText": "Provide additional information about your query performance and timeouts.",
			"required": true
		}
	]
}
---
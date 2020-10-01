<properties
	articleId="problemscopingques-sqlmi-data-import-export-transactionalreplication"
	pageTitle="SQL Database Managed Instance Transactional Replication"
	description="Scoping questions to get more details about data import export transactional replication"
	authors="sojaga"
	authoralias="sojaga"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637312"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "What is the start time of the issue?",
			"required": true
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "What is the end time of the issue? (If ongoing, leave this field blank)",
			"required": false
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
					"value": "modern_platform",
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
			"displayLabel": "Please Provide additional details of your issue",
			"watermarkText": "Please Provide additional information of the issue ",
			"required": true
		}
	]
}
---

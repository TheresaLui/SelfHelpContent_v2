<properties
	pageTitle="Transactional Replication"
	description="Scoping Question for Transactional Replication"
	ms.author="sojaga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630458"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="565e5425-253b-4ea6-8058-85497673007b"
	ownershipId="AzureData_AzureSQLDB"
/>
# Transactional Replication for Azure SQL DB
---

{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"formElements": [
        {
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
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---

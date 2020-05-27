<properties
	pageTitle="Migration tools"
	description="Scoping questions to capture more details about migration tools"
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630433"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-migrating-migration-tools"
	ownershipId="AzureData_AzureSQLDB"
/>
# scoping questions for migration tools
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "Migration tools",
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
    {
            "id": "Tool_dropdown",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the tool being used?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the tool being used",
			      "dropdownOptions": [
                {
                    "value": "DMS",
                    "text": "Database Migration Service (DMS)"
                },
                {
                    "value": "DMA",
                    "text": "Database Migration Assistant (DMA)"
                },
                {
                    "value": "BACPAC",
                    "text": "Export/Import BACPAC"
                },
                {
                    "value": "SSMA",
                    "text": "SQL Server Migration Assistant"
                },
                {
                    "value": "repl",
                    "text": "Transaction replication"
                },
                {
                    "value": "DEA",
                    "text": "Database Experimentation Assistant"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer or other answer"
                }
            ],
            "required": true
        },
    {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error you are receiving. If available,please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---

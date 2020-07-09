<properties
	pageTitle="Planning a migration"
	description="Scoping questions to capture more details about planning a migration"
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630448"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-migrating-to-azure-planning-a-migration"
	ownershipId="AzureData_AzureSQLDB"
/>
# scoping questions for planning a migration
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
            "id": "engine_source",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the DB engine source?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the DB engine source",
	    "dropdownOptions": [
                {
                    "value": "sqlsserver",
                    "text": "SQL Server"
                },
                {
                    "value": "Access",
                    "text": "Access"
                },
                {
                    "value": "DB2",
                    "text": "DB2"
                },
                {
                    "value": "MySQL",
                    "text": "MySQL"
                },
                {
                    "value": "MariaDB",
                    "text": "MariaDB"
                },
                {
                    "value": "ORACLE",
                    "text": "Oracle"
                },
                {
                    "value": "PostgreSQL",
                    "text": "PostgreSQL"
                },
                {
                    "value": "SAPASE",
                    "text": "SAP ASE"
                },
                {
                    "value": "mongodb",
                    "text": "mongoDB"
                },
                {
                    "value": "cassandra",
                    "text": "Cassandra"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer, several engines or not listed"
                }
            ],
            "required": false
        },
  {
            "id": "version",
            "order": 3,
            "controlType": "textbox",
            "visibility": "engine_source != dont_know_answer",
            "displayLabel": "What is the version of the database engine?",
            "infoBalloonText": "Enter the version of the database.",
            "required": false
        },
   {
            "id": "size",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the max size of the largest DB?",
            "infoBalloonText": "Enter the max size of the largest database.",
            "required": false
        },
    {
            "id": "downtime",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the max downtime allowed?",
            "infoBalloonText": "Enter the max downtime allowed for the migration",
            "required": false
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

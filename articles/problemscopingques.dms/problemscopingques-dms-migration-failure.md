<properties
	articleId="C8A6EFC3-5769-44DA-B612-37D78C2B6872"
	pageTitle="DMS Migration failures - scoping questions"
	description="Scoping questions to capture migration failure details"
	authors="radjaram"
	authoralias="rradjou"
	ms.author="radjaram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32673593,32673610,32673597,32673594"
	productPesIds="16307"
	cloudEnvironments="public"
	schemaVersion="1"
	schema="SelfHelpContent"
/>
# Failure when running a database migration using DMS
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "Error when running database migration",
	"fileAttachmentHint": "",
	"formElements": [
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Error when running database migration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },{
			"id": "migrationtype_dropdown",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What is your source and target database combination?",
			"watermarkText": "Select source target pair",
			"infoBalloonText": "If your source target pair is not in the list, choose Other",
			"dropdownOptions": [
				{
					"value": "SQL_Server_To_SQLDB_Offline",
					"text": "SQL Server to Azure SQL Database Offline"
				},{
					"value": "SQL_Server_To_SQLDB_Online",
					"text": "SQL Server to Azure SQL Database Online"
				},{
					"value": "SQL_Server_To_SQLMI_Offline",
					"text": "SQL Server to Azure SQL Database Managed Instance Offline"
				},{
					"value": "SQL_Server_To_SQLMI_Online",
					"text": "SQL Server to Azure SQL Database Managed Instance Online"
				},{
					"value": "RDS_SQL_Server_To_SQLDBOrMI_Online",
					"text": "AWS RDS SQL Server to Azure SQL Database or Managed Instance Online"
				},{
					"value": "MySQL_To_AzureDBForMySQL_Online",
					"text": "MySQL Server to Azure SQL Database for MySQL Online"
				},{
					"value": "RDS_MySQL_To_AzureDBForMySQL_Online",
					"text": "AWS RDS MySQL Server to Azure SQL Database for MySQL Online"
				},{
					"value": "PostgreSQL_To_AzureDBForPostgreSQL_Online",
					"text": "PostgreSQL Server to Azure SQL Database for PostgreSQL Online"
				},{
					"value": "RDS_PostgreSQL_To_AzureDBForPostgreSQL_Online",
					"text": "AWS RDS PostgreSQL Server to Azure SQL Database for PostgreSQL Online"
				},{
					"value": "MongoDB_To_CosmosDBMongoAPI_Offline",
					"text": "MongoDB to Azure Azure CosmosDB Mongo API Offline"
				},{
					"value": "MongoDB_To_CosmosDBMongoAPI_Online",
					"text": "MongoDB to Azure Azure CosmosDB Mongo API Online"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
			}
			],
			"required": true
		},{
			"id":"problem_description",
			"order":1000,
			"controlType":"multilinetextbox",
			"displayLabel":"Please provide additional context for the error message you are encountering.",
			"required":true,
			"useAsAdditionalDetails":true,
			"watermarkText":"Please provide the detailed symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information"
		}
	]
}
---


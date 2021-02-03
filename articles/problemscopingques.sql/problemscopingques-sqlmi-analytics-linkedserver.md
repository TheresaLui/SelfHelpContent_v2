<properties
	articleId="problemscopingques-sqlmi-analytics-linkedserver"
	pageTitle="Scoping questions for linked server in SQL Managed Instance"
	description="Scoping questions to linked server in SQL Managed Instance"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637271"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Linked server errors or questions",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "data_source",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What data source is configured in linked server?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "On-premise SQL Server",
          "text": "On-premise SQL Server is the data source"
        },
        {
          "value": "Azure Synapse SQL",
          "text": " Azure Synapse SQL is the data source"
        },
        {
          "value": "Azure SQL DB/Managed Instance",
          "text": "Azure SQL DB or SQL DB Managed Instance is the data source"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know answer"
        }
      ],
      "required": true
    },
    {
      "id": "configuration_script",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Linked server configuration script",
      "watermarkText": "Please provide the linked server configuration script",
      "required": false
    },
    {
      "id": "error_message",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What error message (if any) are you getting?",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering.",
      "required": true
    }
  ]
}
---
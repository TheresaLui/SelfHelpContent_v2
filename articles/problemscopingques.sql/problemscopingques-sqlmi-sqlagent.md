<properties
	articleId="problemscopingques-sqlmi-sqlagent"
	pageTitle="Scoping questions for SQL Server Agent errors"
	description="Scoping questions to SQL Server Agent errors"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32739490"
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
  "title": "SQL Server Agent errors or questions",
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
      "id": "error_dropdown",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What type of issue are you encountering?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Unable to see SQL Agent",
          "text": "You cannot see SQL Server Agent in SSMS"
        },
        {
          "value": "Unresponsive",
          "text": "Operation in SQL Server Agent is slow or unresponsive"
        },
        {
          "value": "Job History",
          "text": "Job history related issues"
        },
        {
          "value": "SSIS",
          "text": "SSIS job integration issues"
        },
        {
          "value": "Specific Job",
          "text": "Specific agent job issues"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know answer"
        }
      ],
      "required": true
    },
    {
      "id": "problem_description",
      "order": 3,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering.",
      "required": true
    }
  ]
}
---
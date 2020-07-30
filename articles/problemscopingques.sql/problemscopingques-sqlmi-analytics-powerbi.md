<properties
	articleId="problemscopingques-sqlmi-analytics-powerbi"
	pageTitle="Scoping questions for Power BI integration in SQL Managed Instance"
	description="Scoping questions to Power BI integration in SQL Managed Instance"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637292"
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
  "title": "Power BI integration errors or questions in SQL Managed Instance",
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
      "id": "configuration",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Are you using on-premise gateway to connect Managed Instance?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "SMTP server is located in your own on-premise network "
        },
        {
          "value": "No",
          "text": "SMTP server is located in public network"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know answer"
        }
      ],
      "required": true
    },
    {
      "id": "error_message",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What error message (if any) are you getting?",
      "required": false
    },
    {
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
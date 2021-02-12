<properties
	articleId="problemscopingques-sqlmi-analytics-readable-replica"
	pageTitle="Scoping questions for readable replica in SQL Managed Instance"
	description="Scoping questions to readable replica in SQL Managed Instance"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637298"
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
  "title": "Readable replica related errors or questions",
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
      "id": "operations",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What action are you trying to perform?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Enable/Disable",
          "text": "Enable or disable read scale-out in SQL Managed Instance"
        },
        {
          "value": "Connect",
          "text": "Connect to readable replica from client"
        },
        {
          "value": "Monitor",
          "text": "Monitor performance of readable replica"
        },
        {
          "value": "Tempdb",
          "text": "Use tempdb on readable replica"
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
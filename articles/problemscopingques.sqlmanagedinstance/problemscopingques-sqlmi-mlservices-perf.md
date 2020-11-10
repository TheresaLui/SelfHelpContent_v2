<properties
	articleId="problemscopingques-sqlmi-mlservices-perf"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture instance ML Services issues"
	authors="vitomaz-msft"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32742352"
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
  "title": "Performance issues and timeouts",
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
      "id": "problem_end_time",
      "order": 2,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
      "required": false
    },
    {
      "id": "error",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What error are you seeing?",
      "watermarkText": "Please the error message you are encountering",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 4,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering",
      "required": true
    }
  ]
}
---
<properties
	articleId="problemscopingques-sqlmi-servicebroker"
	pageTitle="Scoping questions for service broker errors in SQL Managed Instance"
	description="Scoping questions for service broker errors in SQL Managed Instance"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637305"
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
  "title": "Service Broker errors or questions",
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
      "displayLabel": "What kind of error are you encoutering?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Configuration",
          "text": "Errors when you configure service broker"
        },
        {
          "value": "Message Queue",
          "text": "Message queue is built up or cannot be processed"
        },
        {
          "value": "Conversation Endpoints",
          "text": "Conversation endpoints are unreachable"
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
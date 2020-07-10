<properties
	articleId="problemscopingques-sqlmi-management-monitoring"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture for managed instance management and monitoring"
	authors="zhizhwan"
	authoralias="zhizhwan"
	ms.author="zhizhwan"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637273"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "SQL Database Managed Instance",
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
      "id": "feature_dropdown",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Which feature are you requesting help for?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Diagnostics_Settings",
          "text": "Diagnostics settings can be used to configure streaming of diagnostics telemetry to Azure Storage, Azure Event Hubs, and Azure Monitor logs"
        },
        {
          "value": "Query_Performance_Insights",
          "text": "Query Performance Insights can be used to easily monitor resource usage in your Azure SQL database (single or pooled database) by using build-in monitoring capabilities in the Azure portal"
        },
        {
          "value": "Automatic_Tuning",
          "text": "Automatic tuning automatically recommends and fixes query plan issues, and creates and drops indexes, to improve performance"
        },
        {
          "value": "Alerts_Usage",
          "text": "Alerts can easily be created and managed in the Azure portal"
        },
        {
          "value": "Feature_Other",
          "text": "Other feature not listed"
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
      "watermarkText": "Please provide additional context for your Monitoring, Metrics and Alerts issues.",
      "required": true
    }
  ]
}
---
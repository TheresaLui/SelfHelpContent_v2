<properties
	articleId="problemscopingques-sql-monitor-metrics"
	pageTitle="Azure SQL Database"
	description="Scoping questions to get more details about metrics issue"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32749526"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# Azure SQL Database
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Metrics",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did you face the issue?",
      "required": true
    },
    {
      "id": "type_issue",
      "order": 10,
      "controlType": "dropdown",
      "displayLabel": "What kind of issue are you facing",
      "watermarkText": "Choose an option",
			"dropdownOptions": [
                {
                    "value": "availability",
                    "text": "Metrics not available"
                },
                {
                    "value": "values",
                    "text": "Metrics values"
                },
                {
                    "value": "stream",
                    "text": "Stream or export metrics"
                },
                {
                    "value": "questions",
                    "text": "Questions or advisoring"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
    },
    {
            "id": "available",
            "order": 20,
            "visibility": "type_issue == availability",
            "controlType": "datetimepicker",
            "displayLabel": "Are the metrics available now, if so since when?",
            "required": false
    },
    {
            "id": "interface",
            "order": 30,
            "controlType": "multiselectdropdown",
            "displayLabel": "What interface(s) is being used?",
            "watermarkText": "Choose all the tested interfaces",
			      "dropdownOptions": [
                {
                    "value": "portal",
                    "text": "Azure portal"
                },
                {
                    "value": "powershell",
                    "text": "Powershell"
                },
                {
                    "value": "cli",
                    "text": "Azure CLI"
                },
                {
                    "value": "api",
                    "text": "Rest API"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
    },
    {
            "id": "not_available_at",
            "order": 40,
            "visibility": "type_issue == availability",
            "controlType": "multiselectdropdown",
            "displayLabel": "Where is the metric not available?",
            "watermarkText": "Choose all the options you found",
 			      "dropdownOptions": [
                {
                    "value": "overview",
                    "text": "Resource Overview and Metrics blade"
                },
                {
                    "value": "loganalytics",
                    "text": "Log Analytics"
                },
                {
                    "value": "hubs",
                    "text": "Azure Event Hubs"
                },
                {
                    "value": "storage",
                    "text": "Azure Storage"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
            "id": "destination",
            "order": 50,
            "visibility": "type_issue == stream",
            "controlType": "multiselectdropdown",
            "displayLabel": "What destination is facing the issue?",
            "watermarkText": "Choose all the options you have issues",
 			      "dropdownOptions": [
                {
                    "value": "loganalytics",
                    "text": "Log Analytics"
                },
                {
                    "value": "hubs",
                    "text": "Azure Hubs"
                },
                {
                    "value": "storage",
                    "text": "Azure Storage"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
        {
      "id": "metric",
      "order": 60,
      "controlType": "multilinetextbox",
      "displayLabel": "What metrics are facing the issue?",
      "watermarkText": "Please provide the metrics names",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 99,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering",
      "required": true
    }
  ]
}
---

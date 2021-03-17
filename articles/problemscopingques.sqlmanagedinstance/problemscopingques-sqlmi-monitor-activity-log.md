<properties
	articleId="problemscopingques-sqlmi-monitor-activity-log"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to get more details about activity log issue"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32748861"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Activity Log",
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
                    "value": "view",
                    "text": "View Activity Log data"
                },
                {
                    "value": "operations",
                    "text": "Operations not being recorded"
                },
                {
                    "value": "stream",
                    "text": "Stream Activity Log data"
                },
                {
                    "value": "sqlanalytics",
                    "text": "SQL Analytics"
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
            "id": "interface",
            "order": 20,
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
            "id": "destination",
            "order": 30,
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

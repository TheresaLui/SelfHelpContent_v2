<properties
	articleId="problemscopingques-sql-monitor-alerts"
	pageTitle="Azure SQL Database"
	description="Scoping questions to get more details about alerts issue"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32749523"
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
  "title": "Alerts",
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
                    "text": "View alerts"
                },
                {
                    "value": "crud",
                    "text": "Create, update or delete alerts"
                },
                {
                    "value": "trigger",
                    "text": "Alerts not being triggered"
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
            "id": "triggered",
            "order": 30,
            "visibility": "type_issue == trigger",
            "controlType": "datetimepicker",
            "displayLabel": "When was the last time the alert should have triggered and it wasn't?",
            "required": false
    },
    {
            "id": "notifications",
            "order": 40,
            "visibility": "type_issue == crud || type_issue == trigger",
            "controlType": "multiselectdropdown",
            "displayLabel": "What are the alert notifications?",
            "watermarkText": "Choose all the options being used",
 			      "dropdownOptions": [
                {
                    "value": "email",
                    "text": "Send Email"
                },
                {
                    "value": "sms",
                    "text": "SMS"
                },
                {
                    "value": "push",
                    "text": "Azure App Push Notifications"
                },
                {
                    "value": "voice",
                    "text": "Voice"
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

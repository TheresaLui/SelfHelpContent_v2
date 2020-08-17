<properties
	pageTitle="Error When Connecting to my Database"
	description="Scoping questions to capture more details about connectivity errors 10928, 18456, 40532, 40613, 40615"
	authors="keithelm"
	ms.author="keithelm,muruga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745427,32745428,32745429,32745430,32745431"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="6A45299F-C40E-4CCF-80D1-2ADECF7FF583"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# Error When Connecting to my Database
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Error When Connecting to my Database",
  "fileAttachmentHint": "",
  "diagnosticCard": {
    "title": "SQL DB Connectivity Troubleshooter",
    "description": "The SQL DB Connectivity Troubleshooter can identify the cause of many common service-related connection errors.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "infoBalloonText": "Enter the approximate time you started to see the error.",
      "required": true,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_end_time",
      "order": 2,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
      "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
      "required": false,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_description",
      "order": 1000,
      "controlType": "multilinetextbox",
      "displayLabel": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well.",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "database_name",
      "order": 3000,
      "controlType": "dropdown",
      "displayLabel": "Please provide the database name for which you are creating a support ticket. If multiple databases are affected, select one of the affected databases to start an investigation",
      "required": false,
      "infoBalloonText": "Which of these databases are you filing a ticket for?",
      "dynamicDropdownOptions": {
        "uri": "{resourceId}/databases?api-version=2017-10-01-preview",
        "jTokenPath": "value",
        "textProperty": "name",
        "valueProperty": "id",
        "textPropertyRegex": null,
        "defaultDropdownOptions": {
          "value": "dont_know_answer",
          "text": "Don't know/None of these"
        }
      }
    }
  ]
}
---
